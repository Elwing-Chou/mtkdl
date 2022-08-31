# 深度學習

## Word2Vec

### 資料集

[PTT小資料集](https://drive.google.com/open?id=1BT4h4-kzrtCS_52P2i7C1rlj1GZgEbs6)

[PTT大資料集](https://drive.google.com/open?id=15byko6d_9VJGPOW7DPAN8YiVsleRiURr)

### 標點符號去除

```python
punct = set(u''':!),.:;?]}¢'"、。〉》」』】〕〗〞︰︱︳﹐､﹒﹔﹕﹖﹗﹚﹜﹞！），．：；？｜｝︴︶︸︺︼︾﹀﹂﹄﹏､～￠々‖•·ˇˉ―--′’”([{£¥'"‵〈《「『【〔〖（［｛￡￥〝︵︷︹︻︽︿﹁﹃﹙﹛﹝（｛“‘-—_…~/ －＊➜■─★☆=@<>◉é''')
filter(lambda x: x not in punct, jieba.cut(content))
```

### 網址Regex

```python
content = re.sub(r'https?:\/\/.*[\r\n]*', '', content)
```
### 預處

```python
import re
def process(content):
    content = re.sub(r'https?:\/\/.*[\r\n]*', '', content)
    punct = set(u''':!),.:;?]}¢'"、。〉》」』】〕〗〞︰︱︳﹐､﹒﹔﹕﹖﹗﹚﹜﹞！），．：；？｜｝︴︶︸︺︼︾﹀﹂﹄﹏､～￠々‖•·ˇˉ―--′’”([{£¥'"‵〈《「『【〔〖（［｛￡￥〝︵︷︹︻︽︿﹁﹃﹙﹛﹝（｛“‘-—_…~/ －＊➜■─★☆=@<>◉é''')
    cut = filter(lambda x: x not in punct, jieba.cut(content))
    return " ".join(cut)
df["content"] = df["content"].apply(process)
df
```

## 練習colab(0610)

[w2v](https://colab.research.google.com/drive/1-h_qSJFwfHaJsg2boTX8hIevOSuGqjni?usp=sharing)

[gan](https://colab.research.google.com/drive/14pGRtMZbGZ9wTuVKV2Gof59SP_GEwDUW?usp=sharing)

## 練習colab(0615)

[w2v](https://colab.research.google.com/drive/1lZGTCWwSH-SVJpi_EIhEQqEdfYJWtEZZ?usp=sharing)

[gan](https://colab.research.google.com/drive/1dSHhDukOlkJBwWEzNXBsbxzjQlJHKWcN?usp=sharing)

## 練習colab(1215)

[w2v](https://colab.research.google.com/drive/1ViQxHhPZtGRKDO9ELAXEVux7bAgvY0In?usp=sharing)

[gan](https://colab.research.google.com/drive/1s3mhd7Oa1NvqFQS9cP6VrXjp5PI896Yy?usp=sharing)

## 練習colab(0419)

[w2v](https://colab.research.google.com/drive/1dEuN_e6dT81axdT_QkrWBTCZyKnDfNOo?usp=sharing)

[fasttext](https://colab.research.google.com/drive/1EVt3U7ddQUWokb-ZyZonbsPwkzl-x7O5?usp=sharing)

[gan](https://colab.research.google.com/drive/1QfQpxpzzcm0HtasitGuLhoZ3ZM4yKOkF?usp=sharing)

## 練習colab(0516)

[w2v](https://colab.research.google.com/drive/1N8P6gjZ8Jx5Pm3Ty8lgh7FzFhfOreeeu?usp=sharing)

[fasttext](https://colab.research.google.com/drive/1EVt3U7ddQUWokb-ZyZonbsPwkzl-x7O5?usp=sharing)

[gan](https://colab.research.google.com/drive/1rAMXL6_DntspegCoYspTRW2gnMGFK23d?usp=sharing)

[Face(GPU)](https://colab.research.google.com/drive/1Fdzjw0Rh4ZzRVDvObKAskPAY4AHP-2za?usp=sharing)

## 練習colab(0831)

[w2v](https://colab.research.google.com/drive/1cC0T9L6RSFw7UVJS9BmlBFvh8STuyBZD?usp=sharing)
