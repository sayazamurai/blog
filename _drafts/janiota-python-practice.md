---
title: プログラミング歴ゼロの31歳ジャニヲタ、Pythonを学ぶ。超初心者向けの練習問題を5問紹介。
image: /images/janiota-python-practice/main.jpg
---

![](/images/janiota-python-practice/main.jpg)

こんにちは！ジャニオタ歴20年、アクセサリーデザイナーのSayaと申します。

[いまから始めてみればいいじゃない！Let’s get on！Let’s get on yea！](http://j-lyric.net/artist/a000eac/l00091a.html)ということで、このたび齢31歳にして、プログラミングの勉強を知識ゼロからはじめてみました。

今回は世界平和とジャニヲタの社会的地位向上に貢献すべく、私がプログラミングを学ぶ中で得た知見を、ジャニヲタらしく(？)セクシーにシェアしたいと思います。

## プログラミング歴ゼロの31歳ジャニヲタ、Pythonを学ぶ

最初にどのプログラミング言語を学べば良いのか迷ったので、とりあえず人気投票をチェック(ジャニヲタあるある)。するとPythonという言語が晴れて今年、[プログラミング言語人気ランキング一位を獲得した](https://japan.zdnet.com/article/35104653/)ようなので、Pythonを学ぶことに決めました。

次にPythonを日本語で学ぶか英語で学ぶか迷ったのですが、中学生のころアメリカのHANSONというバンドにハマり、アメリカのファンの方たちとチャットをした経験から、私は英語には抵抗がないので、どうせならと英語で学ぶことに決めました。

プログラマーの友人に英語圏で最も人気のPython教材は何か聞いたところ、「[Learn Python 3 the Hard Way](https://www.amazon.co.jp/Learn-Python-Hard-Way-Introduction-ebook/dp/B07378P8W6)」という入門書が[1200万人](https://learnpythonthehardway.org/book/ex9.html)と、嵐の通算コンサート動員数並みの人数に読まれたらしく、これを使って学ぶことに。

<a href="https://www.amazon.co.jp/Learn-Python-Hard-Way-Introduction-ebook/dp/B07378P8W6/ref=as_li_ss_il?_encoding=UTF8&qid=1508243978&sr=8-3&linkCode=li3&tag=sayajewels-22&linkId=db4bd07c88f288abedebede7db0fe014" target="_blank"><img border="0" src="//ws-fe.amazon-adsystem.com/widgets/q?_encoding=UTF8&ASIN=B07378P8W6&Format=_SL250_&ID=AsinImage&MarketPlace=JP&ServiceVersion=20070822&WS=1&tag=sayajewels-22" ></a><img src="https://ir-jp.amazon-adsystem.com/e/ir?t=sayajewels-22&l=li3&o=9&a=B07378P8W6" width="1" height="1" border="0" alt="" style="border:none !important; margin:0px !important;" />

## 超初心者向けの練習問題を5問紹介

入門書を3分の2くらい読み進めたのはいいものの、本当にスキルが身についているか不安だったので、プログラマーの友人に練習問題をいくつか出してもらいました。苦戦の末に全問解いたあと、友人から「問題と解き方をブログに書いてみるといいよ」と薦められたので、ここで書いてみることにします。

練習問題は5問。全問ジャニーズにちなんだ問題です。想定読者は以下の条件に当てはまる方々です。

- プログラミング歴1週間から1ヶ月以内の超初心者
- 文字列、数値や四則演算、変数、条件分岐、繰り返し、配列(Pythonだとリストやタプル)の使い方を知っている

実行環境はPython 3.6ですが、Python以外の言語を学んでいる方々にも役立てばいいなと思います。

私のような超初心者向けに分かりやすさを重視して書いているので、冗長なのはご理解ください。

## 目次

1. [メンバーの平均年齢を求める](#1)
2. [最年長のメンバーが誰か調べる](#2)
3. [2番目に最年長のメンバーが誰か調べる](#3)
4. [あるメンバーの次に年上のメンバーが誰か調べる](#4)
5. [数年後のメンバーの年齢を正しく求める](#5)

<a name="1"></a>

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

上記のようなリストを入力すると、全員の平均年齢を出力するプログラムを書いてみてください。

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

### Step1: メンバーの年齢の合計値を計算する

メンバーの平均年齢を出すには、まずは全員のメンバーの年齢を合計します。仮に`members`変数が以下だったとすると、

```python
members = [
    ("翔くん", "櫻井翔", 35),
    ("相葉ちゃん", "相葉雅紀", 34),
    ("にの", "二宮和也", 34),
    ("大ちゃん", "大野智", 36),
    ("潤くん", "松本潤", 34)
]
```

年齢はリスト`members`内のタプルの`[2]`の位置に入っているので、以下のようにすれば合計を求められます。

```python
members[0][2] + \
members[1][2] + \
members[2][2] + \
members[3][2] + \
members[4][2]
```

（読みやすさのため複数行に分けて書いているので、その際に必要なバックスラッシュ `\` を使っています)

しかし、これではメンバーが5人より多い、または少ないグループの平均年齢を求めることはできません。

上の式をよく見ると、「リスト`members`に入っている要素を順にとってきて、それぞれの`[2]`の要素を足す」という振り付けが繰り返し行われています。

というわけで、`for`ループを使うのが良さそうです。足し算の結果を`sum_member_age`という変数に保存することにします。

```python
def average_age(members):
    # 1. リスト`members`の要素をとってきて
    for next_member in members:
        # 2. その中の`[2]`の要素を足し、
        #    足し算で得られた結果を変数に保存
        sum_member_age = sum_member_age + next_member[2]
```

しかし、これを実行すると「`sum_member_age`が定義されていない」というエラーが出ます。そこで、ループ処理を行う前に`sum_member_age`に初期値`0`を代入しておくことにします。

```python
def average_age(members):
    # 初期値
    sum_member_age = 0
    for next_member in members:
        sum_member_age = sum_member_age + next_member[2]
```

### Step2: メンバーの年齢の合計値をメンバーの人数で割る

ここまでで年齢の合計値を得ることができたので、次に合計した値をメンバーの数で割って平均値を求めます。

「メンバーの数」はリスト`members`に入っている要素の個数と同じなので`len(members)`で得ることができます。つまり実行したい計算式は以下の通り。

```python
sum_member_age / len(members)
```

これを`return`を使って関数の最後で返すようにします。

```python
def average_age(members):
    sum_member_age = 0
    for next_member in members:
        sum_member_age = sum_member_age + next_member[2]
    return sum_member_age / len(members)
```

完成です！

```python
print(average_age([
    ("翔くん", "櫻井翔", 35),
    ("相葉ちゃん", "相葉雅紀", 34),
    ("にの", "二宮和也", 34),
    ("大ちゃん", "大野智", 36),
    ("潤くん", "松本潤", 34)
]))
```

さっそく嵐のデータを使い、Pythonで実行してみると...

```
❯ python3.6 average_age.py
34.6
```

正しい平均年齢が表示されました！嵐もあと5年ほどで40代なのですね・・・

以上、練習問題その1でした。

<a name="2"></a>

## 練習問題その2: 最年長のメンバーが誰か調べる

では次に、練習問題その1と同じリストを使って、最年長のメンバーが誰かを出力するプログラムを書いてみてください。

実装するのは下の`oldest_member`関数です。嵐のメンバーの場合、最年長は36
歳の大野くんなので、ジャニヲタの愛と親しみを込めてニックネーム"大ちゃん"と出力されればOKです。

```python
def oldest_member(members):
    # ???

# "大ちゃん"と出力されればOK
print(oldest_member([
    ("翔くん", "櫻井翔", 35),
    ("相葉ちゃん", "相葉雅紀", 34),
    ("にの", "二宮和也", 34),
    ("大ちゃん", "大野智", 36),
    ("潤くん", "松本潤", 34)
]))
```

### Step1: 暫定の最年長のメンバーの年齡を保存する

リスト内の最年長のメンバーが誰か調べるには、リストを一番目から順に調べていき、
「今まで調べた中で最年長のメンバーは誰か」をその都度更新する必要があります。最後まで調べたときに最年長だったメンバーが答えというわけです。

ここでも`for`ループが使えそうです。

年齡を比較できるように、暫定の最年長のメンバーの年齡を`oldest_age`という変数に保存することにします。これには初期値として0を代入しておきます。

```python
def oldest_member(members):
    # 暫定の最年長のメンバーの年齡
    oldest_age = 0 # 初期値

    for next_member in members:
        # `oldest_age`を更新していく
```

### Step2: 最年長のメンバーの年齡を更新する

次に、`for`ループの中の「`oldest_age`を更新していく」処理を考えます。

ここでは

- リスト`members`に入っている要素を順にとってきて、それぞれの`[2]`に入っている年齢を、その時点での`oldest_age`と比較する
- 比較した結果`[2]`に入っている年齡の方が`oldest_age`より大きければ、`oldest_age`を`[2]`に入っている年齡に更新する

という処理を最後のメンバーまで繰り返し行います。

```python
def oldest_member(members):
    oldest_age = 0

    for next_member in members:
        # `[2]`に入っている年齢を`oldest_age`と比較する
        if next_member[2] > oldest_age:
            # `[2]`に入っている年齡の方が`oldest_age`
            # より大きければ、`oldest_age`を更新
            oldest_age = next_member[2]
```


### Step3: 最年長のメンバーのニックネームを返す

ここまでの処理で最年長のメンバーの年齡を得ることができました！が、最終的に得たい答えは「最年長のメンバーのニックネーム」です。

そこで、最年長のメンバーのニックネームを`oldest_member_nickname`という変数に保存し、`oldest_age`を更新した時に、同時に更新することにします。初期値として、空の文字列を定義しておきます。

また、`return`を使って、すべてのメンバーの比較が完了した時点での`oldest_member_nickname`を関数の最後で返すようにします。

```python
def oldest_member(members):
    oldest_age = 0
    # 暫定の最年長のメンバーのニックネーム
    oldest_member_nickname = "" #初期値

    for next_member in members:
        if next_member[2] > oldest_age:
            oldest_age = next_member[2]
            # `oldest_age`が更新された時に、
            # `[0]`に入っているニックネームに更新
            oldest_member_nickname = next_member[0]

    # 最終的な最年長のメンバーのニックネームを返す
    return oldest_member_nickname
```

完成です💕

```python
print(oldest_member([
    ("翔くん", "櫻井翔", 35),
    ("相葉ちゃん", "相葉雅紀", 34),
    ("にの", "二宮和也", 34),
    ("大ちゃん", "大野智", 36),
    ("潤くん", "松本潤", 34)
]))
```

嵐のデータを使い、Pythonで実行してみると…

```
❯ python3.6 oldest_member.py
大ちゃん
```

「嵐の最年長メンバーがリーダー大ちゃんである」というジャニヲタ的常識を、プログラミングを使って導き出すことができました😏💙

<a name="3"></a>

## 練習問題その3: 2番目に最年長のメンバーが誰か調べる

次は少しディープな世界に入ります。同じリストを使って、2番目に最年長のメンバーが誰かを出力するプログラムを書いてみてください。

実装するのは下の`second_oldest_member`関数です。嵐のメンバーの場合、大野くんの次に最年長のメンバーはしっかり者な「嵐の次男」的存在、35
歳の櫻井くんなので、"翔くん"と出力されればOKです。

```python
def second_oldest_member(members):
    # ???

# "翔くん"と出力されればOK
print(oldest_member([
    ("翔くん", "櫻井翔", 35),
    ("相葉ちゃん", "相葉雅紀", 34),
    ("にの", "二宮和也", 34),
    ("大ちゃん", "大野智", 36),
    ("潤くん", "松本潤", 34)
]))
```

### step1: 最年長/2番目に最年長のメンバーを保存する

ここでも練習問題その2と同じように`for`ループを使ってリストを一番目から順に調べていく必要がありますが、「今まで調べた中で最年長のメンバーは誰か」に加えて、「今まで調べた中で2番目に最年長のメンバーは誰か」をその都度更新する必要があります。最後まで調べたときに2番目に最年長だったメンバーが答えというわけです。

暫定の最年長のメンバーの年齡`oldest_age`に加えて、暫定の2番目に最年長のメンバーの年齢を`second_oldest_age`という変数に保存し、それぞれに初期値として`0`を代入しておくことにします。

また同様に、暫定の最年長メンバーのニックネーム`oldest_member_nickname`に加えて、2番目に最年長のメンバーのニックネームを`second_oldest_member_nickname`という変数に保存し、それぞれに初期値として空の文字列を定義しておきます。

また、`return`を使って、すべてのメンバーの比較が完了した時点での`second_oldest_member_nickname`を関数の最後で返すようにします。

```python
def second_oldest_member(members):
    # 暫定の最年長のメンバーの年齡
    oldest_age = 0 # 初期値
    # 暫定の2番目に最年長のメンバーの年齡
    second_oldest_age = 0 # 初期値

    # 暫定の最年長のメンバーのニックネーム
    oldest_member_nickname = "" # 初期値
    # 暫定の2番目に最年長のメンバーのニックネーム
    second_oldest_member_nickname = "" # 初期値

    for next_member in members:
        # `oldest_age`/`second_oldest_age`
        # `oldest_member_nickname`/`second_oldest_member_nickname`
        # を更新していく

    # 最終的な2番目に最年長のメンバーのニックネームを返す
    return second_oldest_member_nickname
```

### Step2: 最年長/2番目に最年長のメンバーの年齡を更新する

次に、`for`ループの中の、`oldest_age`、`second_oldest_age`を更新していく処理を考えます。

ここでは練習問題その2で行った「リストからとってきた年齡を`oldest_age`と比較し、更新する」という振り付けに加えて、さらに「リストからとってきた年齡を`second_oldest_age`と比較し、更新する」という振り付けを追加する必要があります。

step by step~~ぶっ飛ぶよりも裸のまま〜(以下省略)~~で考えていきます。

#### Step2-1: メンバーの年齡が、最年長のメンバーより大きい場合

まず

- リスト`members`に入っている要素を順にとってきて、それぞれの`[2]`に入っている年齢を、その時点での`oldest_age`と比較する
- 比較した結果`[2]`に入っている年齡の方が`oldest_age`より大きければ、`oldest_age`を`[2]`に入っている年齡に更新する

ここまでは練習問題その2と全く同じですが、この時点で、それまで`oldest_age`に入っていた年齡は2番目に最年長の年齡ということになるので、さらに

- `second_oldest_age`を**それまでの**`oldest_age`に更新する

という処理を追加します。

```python
def second_oldest_member(members):
    oldest_age = 0
    second_oldest_age = 0

    oldest_member_nickname = ""
    second_oldest_member_nickname = ""

    for next_member in members:
        # `[2]`に入っている年齢を`oldest_age`と比較する
        if oldest_age < next_member[2]:
            # `[2]`に入っている年齡の方が`oldest_age`より大きければ、
            # 1. `oldest_age`を更新
            oldest_age = next_member[2]
            # 2. `second_oldest_age`を更新
            second_oldest_age = oldest_age

    return second_oldest_member_nickname
```

しかしここで少し考えてみましょう🤔

「# 1. 」のステップで `oldest_age`を更新すると、`oldest_age`が**それまでの**`oldest_age`から`[2]`の年齡に置き換わります。この状態で「#2. 」のステップを踏むと、`second_oldest_age`は**更新された後の**`oldest_age`、つまり`[2]`の年齡にじゃまされ、**それまでの**`oldest_age`に置き換えることができなくなってしまいます。まさに[ゆずれないよ誰もじゃまできない](http://j-lyric.net/artist/a000eac/l00091a.html)状態です。

そこで処理の順序を入れ替え、先に`second_oldest_age = oldest_age`を更新してから、`oldest_age`を更新することにします。

```python
def second_oldest_member(members):
    oldest_age = 0
    second_oldest_age = 0

    oldest_member_nickname = ""
    second_oldest_member_nickname = ""

    for next_member in members:
        # `[2]`に入っている年齢を`oldest_age`と比較する
        if oldest_age < next_member[2]:
            # `[2]`に入っている年齡の方が`oldest_age`
            # より大きければ、
            # 1. `second_oldest_age`を更新
            second_oldest_age = oldest_age
            # 2. `oldest_age`を更新
            oldest_age = next_member[2]

    return second_oldest_member_nickname
```

これで問題なく2つの変数を更新することができるようになりました！

#### Step2-2: メンバーの年齡が、最年長のメンバーと同じかそれより小さい場合

では、「比較した結果`[2]`に入っている年齡が`oldest_age`と同じか、`oldest_age`より小さい場合」を考えてみます。

この場合、`oldest_age`を更新する必要はありません。

`second_oldest_age`はどうでしょうか。ここで`[2]`の年齡と`second_oldest_age`の比較が必要になります。

つまり、

- それぞれの`[2]`に入っている年齢を、その時点での`second_oldest_age`と比較する
- 比較した結果`[2]`に入っている年齡の方が`second_oldest_age`より大きければ、`second_oldest_age`を`[2]`に入っている年齡に更新する

という処理を追加します。

```python
def second_oldest_member(members):
    oldest_age = 0
    second_oldest_age = 0

    oldest_member_nickname = ""
    second_oldest_member_nickname = ""

    for next_member in members:
        if next_member[2] > oldest_age:
            second_oldest_age = oldest_age
            oldest_age = next_member[2]

        # `[2]`に入っている年齢が
        # `oldest_age`と同じかそれより小さい場合
        # `[2]`に入っている年齢を
        # `second_oldest_age`と比較する
        elif next_member[2] <= oldest_age and next_member[2] > second_oldest_age:
            # `[2]`に入っている年齡の方が`second_oldest_age`より大きければ、
            # `second_oldest_age`を更新
            second_oldest_age = next_member[2]

    return second_oldest_member_nickname
```

ここまでの処理で、2番目に最年長のメンバーの年齡が分かりました！

# Step3: 最年長/2番目に最年長のメンバーのニックネームを更新する

最終的に得たい答えは2番目に最年長のメンバーのニックネームなので、練習問題その2と同様、`oldest_age`、`second_oldest_age`を更新した時に、`oldest_member_nickname`、`second_oldest_member_nickname`を同時に更新することにします。

ここでも年齡と同様、更新の順序に注意です！

```python
def second_oldest_member(members):
    oldest_age = 0
    second_oldest_age = 0

    oldest_member_nickname = ""
    second_oldest_member_nickname = ""

    for next_member in members:
        if next_member[2] > oldest_age:
            second_oldest_age = oldest_age
            oldest_age = next_member[2]
            # `second_oldest_age`が更新された時に、
            # `second_oldest_member_nickname`を
            # それまでの最年長のメンバーのニックネームに更新
            second_oldest_member_nickname = oldest_member_nickname
            # `oldest_age`が更新された時に、
            # `oldest_member_nickname`を
            # `[0]`に入っているニックネームに更新
            oldest_member_nickname = next_member[0]

        elif next_member[2] <= oldest_age and next_member[2] > second_oldest_age:
            second_oldest_age = next_member[2]
            # `second_oldest_age`が更新された時に、
            # `second_oldest_member_nickname`を
            # `[0]`に入っているニックネームに更新
            second_oldest_member_nickname = next_member[0]

    return second_oldest_member_nickname
```

完成です💕💕

```python
print(oldest_member([
    ("翔くん", "櫻井翔", 35),
    ("相葉ちゃん", "相葉雅紀", 34),
    ("にの", "二宮和也", 34),
    ("大ちゃん", "大野智", 36),
    ("潤くん", "松本潤", 34)
]))
```

嵐のデータを使い、Pythonで実行してみると…

```
❯ python3.6 second_oldest_member.py
翔くん
```

リーダーの長男・大野くんを、しっかり者の次男・櫻井くんが支えていることが、プログラミングでも証明されました😉💙❤️

大野くんと櫻井くんの年長コンビは、漢字の「嵐」の上の部分をとって「山コンビ」と呼ぶという大切なことを最後に付け加えておきます（ジャニヲタ豆知識）。

<a name="4"></a>

## 練習問題その4: あるメンバーの次に年上のメンバーが誰か調べる

<a name="5"></a>

## 練習問題その5: 数年後のメンバーの年齢を正しく求める




