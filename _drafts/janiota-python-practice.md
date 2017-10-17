---
title: プログラミング歴ゼロの31歳ジャニヲタ、Pythonを学ぶ。超初心者向けの練習問題を5問紹介。
image: /images/janiota-python-practice/main.jpg
---

![](/images/janiota-python-practice/main.jpg)

こんにちは！ジャニオタ歴20年、アクセサリーデザイナーのSayaと申します。

[いまから始めてみればいいじゃない！Let’s get on！Let’s get on yea！](http://j-lyric.net/artist/a000eac/l00091a.html)ということで、このたび齢31歳にして、プログラミングの勉強を知識ゼロからはじめてみました。

今回は世界平和とジャニオタの社会的地位向上に貢献すべく、私がプログラミングを学ぶ中で得た知見を、ジャニオタらしく(？)セクシーにシェアしたいと思います。

## プログラミング歴ゼロの31歳ジャニヲタ、Pythonを学ぶ

最初にどのプログラミング言語を学べば良いのか迷ったので、とりあえず人気投票をチェック(ジャニオタあるある)。するとPythonという言語が晴れて今年、[プログラミング言語人気ランキング一位を獲得した](https://japan.zdnet.com/article/35104653/)ようなので、Pythonを学ぶことに決めました。

次にPythonを日本語で学ぶか英語で学ぶか迷ったのですが、中学生のころアメリカのHANSONというバンドにハマり、アメリカのファンの方たちとチャットをした経験から、私は英語には抵抗がないので、どうせならと英語で学ぶことに決めました。

プログラマーの友人に英語圏で最も人気のPython教材は何か聞いたところ、「[Learn Python 3 the Hard Way](https://www.amazon.co.jp/Learn-Python-Hard-Way-Introduction-ebook/dp/B07378P8W6)」という入門書が[1200万人](https://learnpythonthehardway.org/book/ex9.html)と、嵐の年間コンサート動員数並みの人数に読まれたらしく、これを使って学ぶことに。

<a href="https://www.amazon.co.jp/Learn-Python-Hard-Way-Introduction-ebook/dp/B07378P8W6/ref=as_li_ss_il?_encoding=UTF8&qid=1508243978&sr=8-3&linkCode=li3&tag=sayajewels-22&linkId=db4bd07c88f288abedebede7db0fe014" target="_blank"><img border="0" src="//ws-fe.amazon-adsystem.com/widgets/q?_encoding=UTF8&ASIN=B07378P8W6&Format=_SL250_&ID=AsinImage&MarketPlace=JP&ServiceVersion=20070822&WS=1&tag=sayajewels-22" ></a><img src="https://ir-jp.amazon-adsystem.com/e/ir?t=sayajewels-22&l=li3&o=9&a=B07378P8W6" width="1" height="1" border="0" alt="" style="border:none !important; margin:0px !important;" />

## 超初心者向けの練習問題を5問紹介

入門書を3分の2くらい読み進めたのはいいものの、本当にスキルが身についているか不安だったので、プログラマーの友人に練習問題をいくつか出してもらいました。苦戦の末に全問解いたあと、友人から「問題と解き方をブログに書いてみるといいよ」と薦められたので、ここで書いてみることにします。

練習問題は5問。全問ジャニーズにちなんだ問題です。想定読者は以下の条件に当てはまる方々です。

- プログラミング歴1週間から1ヶ月以内の超初心者
- 文字列、数値や四則演算、変数、条件分岐、繰り返し、配列(Pythonだとリストやタプル)の使い方を知っている

実行環境はPython 3.6ですが、Python以外の言語を学んでいる方々にも役立てばいいなと思います。

## 練習問題の目次

1. メンバーの平均年齢を求める
2. 最年長のメンバーが誰か調べる
3. 2番目に最年長のメンバーが誰か調べる
4. あるメンバーの次に年上のメンバーが誰か調べる
5. 数年後のメンバーの年齢を正しく求める

## 練習問題その1: メンバーの平均年齢を求める

まずはウォーミングアップとして、[You are my SOUL！SOUL！いつもすぐそばにある！](http://j-lyric.net/artist/a000eac/l00091a.html)今をときめくジャニーズの財務基盤、嵐先生の平均年齢を、Pythonを使って求めてみましょう。

嵐のメンバーのニックネーム・フルネームと2017年10月現在の年齢はこちらです。まさかご存知ない方はいないと思いますが、念のため。順番は適当です。

| ニックネーム | フルネーム | 年齢 |
|------------|------------|:------------:|
| 翔くん | 櫻井 翔 | 35 |
| 相葉ちゃん | 相葉 雅紀 | 34 |
| にの | 二宮 和也 | 34 |
| 大ちゃん | 大野 智 | 36 |
| 潤くん | 松本 潤 | 34 |

翔くんは11月で36歳になりますね！翔くんおめでとう！！（若干のフライング）

### データをPythonで表現

上の表をPythonで表現してみると、こうなります。

```python
[
    ("翔くん", "櫻井翔", 35),
    ("相葉ちゃん", "相葉雅紀", 34),
    ("にの", "二宮和也", 34),
    ("大ちゃん", "大野智", 36),
    ("潤くん", "松本潤", 34)
]
```

「A, B, C」といったデータの羅列をPythonで表現する際、

- A, B, Cがそれぞれ違う系統のデータの場合はタプル `(A, B, C)` を使う
- A, B, Cがそれぞれ同じ系統のデータの場合はリスト `[A, B, C]` を使う

という決まりがあるので、「ニックネーム、フルネーム、年齢」は違う系統のデータのためタプルで表現し、そのタプルの羅列は同じ系統のデータのためリストで表現しています。

### 練習問題その1

上記のようなリストを入力すると、全員の平均年齢を出力するプログラムを書いてみてください。これが練習問題その1です。

具体的には、下の`average_age`関数を実装してください。嵐のメンバーの場合、平均年齢は`(35+34+34+36+34)/5` = 34.6歳なので、34.6と出力されればOKです。

```python
def average_age(members):
    # ???

# 34.6と表示されればOK
print(average_age([
    ("翔くん", "櫻井翔", 35),
    ("相葉ちゃん", "相葉雅紀", 34),
    ("にの", "二宮和也", 34),
    ("大ちゃん", "大野智", 36),
    ("潤くん", "松本潤", 34)
]))
```

以下、解き方を[step by step~~ブッ飛ぶよりも裸のまま突っ込め~~](http://j-lyric.net/artist/a000eac/l00091a.html)で説明していきます。

### Step2: メンバーの年齢の合計値を計算する

ここからは関数'sexy_average'の中身を考えていきます。

平均年齢を出すには、まずは

1. 全員のメンバーの年齢を合計

して合計値を得る必要があります。

関数`sexy_average`で最終的に得たい合計値を`sum_member_age`というニックネームの変数としておきます。

```python
def sexy_average(members):

    (1)???

    sum_member_age = (2)???

    (3)???

print(sexy_average(対象メンバーのデータ))
```

`(対象メンバーのデータ)`には、後から上で作った嵐のデータのリストを置き換えます。
つまり

```python
members =
対象メンバーのデータ =
[("翔くん", "櫻井翔", 35),
("相葉ちゃん", "相葉雅紀", 34),
("にの", "二宮和也", 34),
("大ちゃん", "大野智", 36),
("潤くん", "松本潤", 34)]
```

です。

では`sum_member_age`を得られるまでの`(1)???`、`(2)???`には何を入れればよいか考えていきます。

ここで最終的に得たい`sum_member_age`は嵐の全員のメンバーの年齢の合計値です。

これをpython的に式にすると、年齢はリスト`members`内のタプルの`[2]`の位置に入っているので、

```python
sum_member_age = members[0][2] + members[1][2] + members[2][2] + members[3][2] + members[4][2]
```

となります。

この計算式をそのまま実行しても`sum_member_age`を得ることはできますが、後からメンバーを置き換えて処理を実行することができません。何より、あまりにもセクシーではありません！！😵

上の式で処理されているのがどんな内容かを考えてみることにします。上の式をよく見ると

* リスト`members`の最初の要素`("翔くん", "櫻井翔", 35)`に入っている`[2]`の要素を足す
* さらにリスト`members`の2番目の要素`("相葉ちゃん", "相葉雅紀", 34)`に入っている`[2]`の要素を足す
* さらにリスト`members`の3番目の要素`("にの", "二宮和也", 34)`に入っている`[2]`の要素を足す
.
.

というように、「リスト`members`に入っている要素を順にとってきて、`[2]`の要素を足す」という処理が繰り返し行われています。繰り返し処理を使うのがセクシーそうです！

`for`を使って

1. リスト`members`の要素をとってきて
2. その中の`[2]`の要素を足し
3. 足し算で得られた結果を`sum_member_age`に置き換える

の3つを繰り返し行う処理を作ってみることにします。

まずは「1. リスト`members`の要素を順にとってきて」の部分を考えます。後でとってきた要素をつかって2. 、3. 、の処理を行いたいので、変数を作って`members`からとってきた要素を一旦この変数に入れておきます。

変数にはメンバーのデータが順に渡されていくので`next_member`というニックネームをつけました。

```python
def sexy_average(members):
    for next_member in members:
　　
    sum_member_age = (2)???

    (3)???

print(sexy_average(対象メンバーのデータ))
```

次に「2. (とってきた要素の中の)`[2]`の要素を足し」、「3. 足し算で得られた結果を`sum_member_age`に置き換える」の部分を考えます。

足し算をするには「足されるもの」が必要ですが、「足されるもの」は、その前のメンバーの足し算で得られた結果`sum_member_age`なので、この部分は

```python
sum_member_age + next_member[2]
```

の数式で計算できます。

この数式で得られた計算結果を`sum_member_age`に置き換えます。

```python
sum_member_age = sum_member_age + next_member[2]
```

これで2. 、3. の処理を行う数式ができました！この数式を、1. で作った`for`の中に入れ、最後のメンバーまで処理を繰り返し実行すると、最終的な`sum_member_age`を得ることができるはずです。

```python
def sexy_average(members):
    for next_member in members:
        sum_member_age = sum_member_age + next_member[2]
　　　　　
　　 (3)???

print(sexy_average(対象メンバーのデータ))
```

ループ処理が完成しました！

これがうまくいくかを実験してみます。

まず

```python
for members in members:
```

によって、最初に変数`member`にリスト`members`の最初の要素、つまり`("翔くん", "櫻井翔", 35)`が渡されます。

次に

```python
sum_member_age = sum_member_age + next_member[2]
```

によって足し算が実行されます...が、ここでさっそく問題があります。この段階では`sum_member_age`に何も値が定義されていないため、最初の足し算が実行できません！

そこで、ループ処理を行う前に`sum_member_age`に仮の値`0`を定義しておくことにします。

```python
def sexy_average(members):
    sum_member_age = 0
    for member in members:
　　 sum_member_age = sum_member_age + next_member[2]

　　 (3)???

print(sexy_average(対象メンバーのデータ))
```

こうすることで、memberに最初の要素`("翔くん", "櫻井翔", 35)`が渡された時に、無事以下の式が実行されます。

```python
sum_member_age = 0 + 35
```

さらに`sum_member_age`が`0 + 35`の結果、
つまり35に置き換わります。

```python
sum_member_age = 35
```

これで最初のループ処理が完了したので、次のメンバーにうつり、`member`にリスト`members`の2番目の要素`("相葉ちゃん", "相葉雅紀", 34)`が渡されます。

最初のループ処理で`sum_member_age`は35に置き換わっているので、ここで行われる足し算は以下のようになります。

```python
sum_member_age = 35 + 34
```

さらに`sum_member_age`が`35 + 34`の結果、
つまり69に置き換わります。

```python
sum_member_age = 69
```

この処理をリスト`members`の最後の要素`("潤くん", "松本潤", 34)`まで繰り返すと、最終的に得られる`sum_number_age`は173となります。

```python
sum_member_age = 173
```

嵐の全員のメンバーの年齢の合計値が173であることが分かりました！

#### Step3: メンバーの年齢の合計値をメンバーの人数で割る

```python
def sexy_average(members):
    sum_member_age = 0
    for member in members:
　　 sum_member_age = sum_member_age + next_member[2]

　　 (3)???

print(sexy_average(対象メンバーのデータ))

ここまでで年齢の合計値を得ることができたので、次に`(3)???`に入る処理、つまり

2. 合計した値をメンバーの数で割る

を考えていきます。

「メンバーの数」はリスト`members`に入っている要素の個数と同じなので`len(members)`で得ることができます。

つまり実行したい計算式は

```python
sum_member_age / len(members)
```

となります。

`対象メンバーのデータ`が嵐のメンバーのデータ場合、`len(members)`は5となるので

上の数式では

```python
173 / 5
```

がの数式が計算されます。

この数式の計算結果を、`return`を使って最終的に関数`sexy_average`で返すようにします。

```python
def sexy_average(members):
    sum_member_age = 0
    for member in members:
　　 sum_member_age = sum_member_age + member[2]

　　 return sum_member_age / len(members)

print(sexy_average(対象メンバーのデータ))
```

これで実行したいすべての処理を表現できました！

`対象メンバーのデータ`に嵐のメンバーのデータのリストを置き換えて

```python
def sexy_average(members):
    sum_member_age = 0
    for next_member in members:
        sum_member_age = sum_member_age + next_member[2]

    return sum_member_age / len(members)

print(sexy_average([
    ("翔くん", "櫻井翔", 35),
    ("相葉ちゃん", "相葉雅紀", 34),
    ("にの", "二宮和也", 34),
    ("大ちゃん", "大野智", 36),
    ("潤くん", "松本潤", 34)
]))
```

これをpython3.6で実行してみると...

```
~/Documents/code/learn-python master*
❯ python3.6 ex32_2/average_age.py
34.6
```

嵐のメンバーの平均年齢は34.6歳であることが分かりました！！！やったやったー！！

