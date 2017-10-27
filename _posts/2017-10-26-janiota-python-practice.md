---
title: プログラミング歴ゼロの31歳ジャニヲタ、Pythonを学ぶ。超初心者向けの練習問題を5問紹介。
image: /images/janiota-python-practice/IMG_0083.jpg
---

<figure>
    <img src="/images/janiota-python-practice/IMG_0083.jpg" />
    <figcaption>

    </figcaption>
</figure>

こんにちは！ジャニヲタ歴20年、アクセサリーデザイナーのSayaと申します。

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

<figure>
    <img src="/images/janiota-python-practice/IMG_0088.jpg" />
    <figcaption>

    </figcaption>
</figure>

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

<figure>
    <img src="/images/janiota-python-practice/IMG_0181.jpg" />
    <figcaption>

    </figcaption>
</figure>


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

<figure>
    <img src="/images/janiota-python-practice/IMG_2125.jpg" />
    <figcaption>

    </figcaption>
</figure>

次は少しディープな世界に入ります。同じリストを使って、2番目に最年長のメンバーが誰かを出力するプログラムを書いてみてください。

実装するのは下の`second_oldest_member`関数です。嵐のメンバーの場合、大野くんの次に最年長のメンバーはしっかり者な「嵐の次男」的存在、35
歳の櫻井くんなので、`翔くん`と出力されればOKです。

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

### step1: 暫定の最年長/2番目に最年長のメンバーを保存する

ここでも練習問題その2と同じように`for`ループを使ってリストを一番目から順に調べていく必要がありますが、「今まで調べた中で最年長のメンバーは誰か」に加えて、**「今まで調べた中で2番目に最年長のメンバーは誰か」**をその都度更新する必要があります。最後まで調べたときに2番目に最年長だったメンバーが答えというわけです。

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

step by step~~ブッ飛ぶよりも裸のまま〜(以下省略)~~で考えていきます。

#### Step2-1: メンバーの年齡が、最年長のメンバーより大きい場合

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

「# 1. 」のステップで `oldest_age`を更新すると、`oldest_age`が**それまでの**`oldest_age`から`[2]`の年齡に置き換わります。この状態で「#2. 」のステップを踏むと、`second_oldest_age`は**更新された後の**`oldest_age`、つまり`[2]`の年齡にはばまれ、**それまでの**`oldest_age`に置き換えることができなくなってしまいます。まさに[ゆずれないよ誰もじゃまできない](http://j-lyric.net/artist/a000eac/l00091a.html)状態です。

そこで処理の順序を入れ替え、先に`second_oldest_age`を更新してから、`oldest_age`を更新することにします。

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
        elif next_member[2] <= oldest_age and \
        next_member[2] > second_oldest_age:
            # `[2]`に入っている年齡の方が`second_oldest_age`より大きければ、
            # `second_oldest_age`を更新
            second_oldest_age = next_member[2]

    return second_oldest_member_nickname
```

これで、2番目に最年長のメンバーの年齡が分かりました！

### Step3: 最年長/2番目に最年長のメンバーのニックネームを更新する

最終的に得たい答えは2番目に最年長のメンバーのニックネームなので、練習問題その2と同様、`oldest_age`、`second_oldest_age`を更新した時に、`oldest_member_nickname`、 `second_oldest_member_nickname` を同時に更新することにします。

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

**大野くんと櫻井くんの年長コンビは、漢字の「嵐」の上の部分をとって「山コンビ」と呼ぶ**という大切なことを最後に付け加えておきます（ジャニヲタ豆知識）。

<a name="4"></a>

## 練習問題その4: あるメンバーの次に年上のメンバーが誰か調べる

<figure>
    <img src="/images/janiota-python-practice/IMG_009.jpg" />
    <figcaption>
    </figcaption>
</figure>

さらにディープな世界に入ります。次は「あるメンバーの次に年上のメンバーが誰かを出力するプログラムを書いてください。」という問題です。

嵐の**「山コンビ」**が[涙を禁じ得ない数々のエピソード](https://matome.naver.jp/odai/2138017494743524101)を生み出してきたように、そして櫻井くんとその次に年長の相葉くんの**「櫻葉コンビ」**が[笑いを堪えきれない数々の珍事](https://matome.naver.jp/odai/2138130307173050501)を生み出してきたように、グループの~~萌えポイント~~ターニングポイントにはいつも「年の近いメンバー同士のコンビ」の存在があります。

刻々と紡がれるジャニーズヒストリーの中で重要な事件を見逃さないよう、このコンビを各グループごとに把握しておくことはジャニヲタの必須要件です。

嵐についてはすでに多くの事件が詳細な記録とともに残されているので、ここでは東京オリンピックの頃にはきっと時代が追いついているであろう、ポテンシャルを秘めまくったジャニーズの次世代グループ「Se<span class="color-red-600">xy</span> Zone」のメンバーを使って、コードとともに未知の世界を解明することにします。

Se<span class="color-red-600">xy</span> Zoneのメンバーのニックネーム・フルネームと2017年10月現在の年齢はこちらです。さあ、未知の世界[「Se<span class="color-red-600">xy</span>世代」](http://j-lyric.net/artist/a055cda/l026e0d.html)へ🥀

| ニックネーム | フルネーム | 年齢 |
|------------|------------|:------------:|
| 聡ちゃん | 松島　聡 | 19 |
| マリ | マリウス 葉 | 17 |
| ケンティー | 中島　健人 | 23 |
| 風磨くん | 菊池　風磨 | 22 |
| 勝利くん | 佐藤　勝利 | 20 |

上の表をPythonで表現してみると、こうなります。

```python
[
    ("聡ちゃん", "松島聡", 19),
    ("マリ", "マリウス葉", 17),
    ("ケンティー", "中島健人", 23),
    ("風磨くん", "菊池風磨", 22),
    ("勝利くん", "佐藤勝利", 20)
]
```

### `next_older_member`関数

実装するのは下の`next_older_member`関数です。対象のメンバー`members`に加え、「あるメンバー」のニックネームを指定できるよう`nickname`という変数を追加します。

たとえば`nickname`に`"風磨くん"`と指定した場合、22歳の菊池風磨くんの次に年上の`ケンティー`と出力されればOKです。

```python
# 変数`nickname`を追加
def next_older_member(members, nickname):
    # ???

# "ケンティー"と出力されればOK
print(next_older_member([
    ("聡ちゃん", "松島聡", 19),
    ("マリ", "マリウス葉", 17),
    ("ケンティー", "中島健人", 23),
    ("風磨くん", "菊池風磨", 22),
    ("勝利くん", "佐藤勝利", 20)
], "風磨くん"))
```

### Step1: 「あるメンバー」の年齡を保存する

まずは、`nickname`に指定された「あるメンバー」の年齡を求める必要があります。後にこの年齡と各メンバーの年齡を比較していくので、これを`compared_age`という変数に保存し、初期値`0`を代入しておきます。

`for`ループを使って、リスト`members`の`[0]`に入っているニックネームが`nickname`と一致した時に、`compared_age`を`members`の`[2]`に入っている年齡に更新する処理を行います。

```python
def next_older_member(members, nickname):
    # `nickname`に指定されたメンバーの年齡
    compared_age = 0 # 初期値

    # `members`のニックネームが`nickname`と一致した時に
    # `compared_age`を`members`の年齡に更新
    for next_member in members:
        if next_member[0] == nickname:
            compared_age = next_member[2]
```

`compared_age`が正しく指定されているかどうか、`print`を使って確かめてみましょう。上記の最後に`print`を追加し、`nickname`に`"風磨くん"`と指定して実行してみます。

```python
def next_older_member(members, nickname):
    # ...

    print(compared_age)

print(next_older_member([
    ("聡ちゃん", "松島聡", 19),
    ("マリ", "マリウス葉", 17),
    ("ケンティー", "中島健人", 23),
    ("風磨くん", "菊池風磨", 22),
    ("勝利くん", "佐藤勝利", 20)
], "風磨くん"))
```

実行すると、風磨くんの年齡である`22`が出力されました。

```
❯ python3.6 next_older_member.py
22
```

これで「あるメンバー」の年齡を`compared_age`に保存することができました！

次のステップに進む前に、`print`は消しておきます。

### Step2: 「次に年上のメンバー」を保存する

次に、これまでの練習問題と同じように`for`ループを使って、各メンバーの年齡を`compared_age`と順に比較していく処理を考えます。

求めたい「次に年上のメンバー」の年齡を変数`next_older_member_age`に、ニックネームを変数`next_older_member_nickname`に保存し、それぞれに初期値`0`と空の文字列を代入しておくことにします。

また、ループ処理の中で条件が満たされた時に`next_older_member_age`を今調べているメンバーの年齡に更新し、同時に`next_older_member_nickname`を今調べているメンバーのニックネームに更新します。

さらに、`return`を使って、すべてのメンバーの比較が完了した時点での`next_older_member_nickname`を関数の最後で返すようにします。

```python
def next_older_member(members, nickname):
    # ... (compared_ageを指定、省略)

    # 「次に年上のメンバー」の年齡
    next_older_member_age = 0 # 初期値
    # 「次に年上のメンバー」のニックネーム
    next_older_member_nickname = "" #初期値

    for next_member in members:
        # 条件が満たされた時に
        if # ???:
            # `next_older_member_age`を更新
            next_older_member_age = next_member[2]
            # `next_older_member_nickname`を更新
            next_older_member_nickname = next_member[0]

    # 最終的な「次に年上のメンバー」のニックネームを返す
    return next_older_member_nickname
```

### Step3: 「次に年上のメンバー」を更新する

では`next_older_member_age`を更新するのは、どんな条件がそろった時でしょうか。

まず、「次に年上のメンバー」の年齡は必ず「あるメンバー」の年齡より大きいので、

1\. `members`の`[2]`に入っている年齡が`compared_age`より大きい

という条件が必要です。

さらに、**その時点での**「次に年上のメンバー」と今調べているメンバーの年齡を比較し、**その時点での**「次に年上のメンバー」の方が大きければ、「次に年上のメンバー」は今調べているメンバーに置き換わることになるので

2\. `next_older_member_age`が`members`の`[2]`に入っている年齡より大きい

という条件も同時に満たす必要があります。

今調べているメンバーの年齡が、**その時点での**「次に年上のメンバー」の年齡と、「あるメンバー」の年齡の間にある時に、`next_older_member_age`を更新する、というわけです😉

```python
def next_older_member(members, nickname):
    # ...

    next_older_member_age = 0
    next_older_member_nickname = ""

    for next_member in members:
        # 1. `members`の`[2]`に入っている年齡が
        # `compared_age`より大きく
        # 2. `next_older_member_age`が
        # ` members`の`[2]`に入っている年齡より大きい場合
        if next_member[2] > compared_age and \
        next_older_member_age > next_member[2]:
            # `next_older_member_age`を更新する
            next_older_member_age = next_member[2]
            next_older_member_nickname = next_member[0]

    return next_older_member_nickname
```

さっそく実行してみましょう！

```python
# "ケンティー"と出力されればOK
print(next_older_member([
    ("聡ちゃん", "松島聡", 19),
    ("マリ", "マリウス葉", 17),
    ("ケンティー", "中島健人", 23),
    ("風磨くん", "菊池風磨", 22),
    ("勝利くん", "佐藤勝利", 20)
], "風磨くん"))
```

しかし、実行してみると、出力されたのは空の文字列だけ。どこが間違っているのでしょうか？

```
❯ python3.6 next_older_member.py



```


### Step4: `next_older_member_age`のバグを直す

```python
def next_older_member(members, nickname):
    # ...

    next_older_member_age = 0
    next_older_member_nickname = ""

    for next_member in members:
        if next_member[2] > compared_age and \
        next_older_member_age > next_member[2]:
            next_older_member_age = next_member[2]
            next_older_member_nickname = next_member[0]

    return next_older_member_nickname
```

上記の`for`の中身について、少し考えてみましょう🤔[~~大人の~~最初にきめたやり方それが正解なの？](http://j-lyric.net/artist/a055cda/l026e0d.html)

最初に定義しておいた`next_older_member_age`の初期値`0`はどのメンバーよりも年上ではありません。これでは、2番目の`for`ループの中にある、

```python
if next_member[2] > compared_age and \
    next_older_member_age > next_member[2]:
```

上の二行目の「`next_older_member_age`が`members`の`[2]`に入っている年齡より大きい」という条件は未来永劫、満たされることはありません。

だから、`next_older_member_age`は`0`のまま、`next_older_member_nickname`は空の文字列のままになってしまっているのです。

```python
if next_member[2] > compared_age and \
    next_older_member_age > next_member[2]:
```

そこで一行目の「`next_older_member_age`が`members`の`[2]`に入っている年齡より大きい」という条件を満たす最初のメンバーが現れた時に、`next_older_member_age`がそのメンバーの年齡に必ず置き換わるように、`next_older_member_age`の初期値には**どのメンバーの年齡よりも大きい値**を代入しておく必要があります。

100歳までアイドルを続けているメンバーはどのグループにもさすがにいないので、`next_older_member_age`の初期値には`100`を代入しておくことにします。

```python
def next_older_member(members, nickname):
    compared_age = 0

    for next_member in members:
        if next_member[0] == nickname:
            compared_age = next_member[2]

    next_older_member_age = 100 # 初期値を変更
    next_older_member_nickname = ""

    for next_member in members:
        if next_member[2] > compared_age and next_older_member_age > next_member[2]:
            next_older_member_age = next_member[2]
            next_older_member_nickname = next_member[0]

    return next_older_member_nickname
```

これで無事、最後のメンバーまで比較を行うことができるようになりました😘完成です🌹💕

```python
print(oldest_member([
    ("聡ちゃん", "松島聡", 19),
    ("マリ", "マリウス葉", 17),
    ("ケンティー", "中島健人", 23),
    ("風磨くん", "菊池風磨", 22),
    ("勝利くん", "佐藤勝利", 20)
], "風磨くん"))
```

Se<span class="color-red-600">xy</span> Zoneのデータを使い、`nickname`に`"風磨くん"`と指定してPythonで実行してみると…

```
❯ python3.6 next_older_member.py
ケンティー
```

さらに`nickname`に`"マリ"`と指定してPythonで実行してみると…

```
❯ python3.6 next_older_member.py
聡ちゃん
```

これで我々は風磨くんとケンティーの「ふまけん💜💙」コンビ、マリと聡ちゃんの「聡マリ💚💛」コンビがこれから刻む**[新しいAge](http://j-lyric.net/artist/a055cda/l026e0d.html)**を見逃さずに済みそうです。来たるSe<span class="color-red-600">xy</span>時代への大きな一歩を踏み出すことができました😉🥀

<a name="5"></a>

## 練習問題その5: 数年後のメンバーの年齢を正しく求める

<figure>
    <img src="/images/janiota-python-practice/IMG_3824.jpg" />
    <figcaption>

    </figcaption>
</figure>

いよいよ最後の問題です。またここにSe<span class="color-red-600">xy</span> Zoneのメンバーのデータを用意しました。一番右の行は3年後、東京オリンピックの年のメンバーの年齡です。ちょうど時代が追いついている頃です。

| ニックネーム | フルネーム | 年齢 | 3年後 |
|------------|------------|:------------:|:------------:|
| 聡ちゃん | 松島　聡 | 19 | 22 |
| マリ | マリウス 葉 | 17 | 20 |
| ケンティー | 中島　健人 | 23 | 26 |
| 風磨くん | 菊池　風磨 | 22 | 25 |
| 勝利くん | 佐藤　勝利 | 20 | 22 |

ここで一人、3年後の年齡が間違っているメンバーがいます。誰でしょう…🤔

| ニックネーム | フルネーム | 年齢 | 3年後 |
|------------|------------|:------------:|:------------:|
| 聡ちゃん | 松島　聡 | 19 | 22 |
| マリ | マリウス 葉 | 17 | 20 |
| ケンティー | 中島　健人 | 23 | 26 |
| 風磨くん | 菊池　風磨 | 22 | 25 |
| 勝利くん | 佐藤　勝利 | 20 | <span class="red">✗ 22</span><br><span class="green">◯ 23</span> |

勝利くんの年齡が間違っています。**[新しいAge](http://j-lyric.net/artist/a055cda/l026e0d.html)**を間違ってはいけません！

### `check_future_age`関数

最後の問題では、`check_future_age`という関数を実装してもらいます。この関数には、メンバーの現在の情報と、「何年後」かの情報を引数として指定します。そして「何年後」かの情報は、年齡が正しい場合と、間違っている場合があります。

こちらは3年後の情報を2つめの引数にしています。このように、正しい「何年後」かの情報を渡した場合、`check_future_age`は`True`を返します。

```python
print(check_future_age(
    [
        ("聡ちゃん", "松島聡", 19),
        ("マリ", "マリウス葉", 17),
        ("ケンティー", "中島健人", 23),
        ("風磨くん", "菊池風磨", 22),
        ("勝利くん", "佐藤勝利", 20)
    ],
    # 正しい3年後の年齡
    [
        ("聡ちゃん", "松島聡", 22),
        ("マリ", "マリウス葉", 20),
        ("ケンティー", "中島健人", 26),
        ("風磨くん", "菊池風磨", 25),
        ("勝利くん", "佐藤勝利", 23)
    ]
))

# → Trueと出力
```

また、以下のように間違った情報を渡した場合、`check_future_age`は`False`を返します。

```python
print(check_future_age(
    [
        ("聡ちゃん", "松島聡", 19),
        ("マリ", "マリウス葉", 17),
        ("ケンティー", "中島健人", 23),
        ("風磨くん", "菊池風磨", 22),
        ("勝利くん", "佐藤勝利", 20)
    ],
    # 間違った3年後の年齡
    [
        ("聡ちゃん", "松島聡", 22),
        ("マリ", "マリウス葉", 20),
        ("ケンティー", "中島健人", 26),
        ("風磨くん", "菊池風磨", 25),
        # ↓正しくは23歳
        ("勝利くん", "佐藤勝利", 22)
    ]
))

# → Falseと出力
```

メンバーの順番はひとつめの引数とふたつめの引数で変わりません。それでは、この`check_future_age`関数を書いてみましょう。

```python
def check_future_age(current_members, future_members):
    # future_membersの年齡が、current_membersの年齡の
    # 「何年後」かの年齡を正しく表していたらTrueを返し、
    # そうでなければFalseを返す
```

### Step1: 何を比較するかを考える

まずは、ひとつめの引数のリストとふたつめの引数のリスト、それぞれのリスト内の要素の`[2]`に入っている年齡を比べ、差を計算する必要があります。

この**引数間の年齡の差**が、すべてのメンバーについて同じであれば`True`を、1人でも違えば`False`を返すようにすればよさそうです。

```python
# 正しい例

# 聡ちゃんの年齢差は3
("聡ちゃん", "松島聡", 19)
("聡ちゃん", "松島聡", 22)

# マリの年齢差も3で、聡ちゃんと同じ
("マリ", "マリウス葉", 17)
("マリ", "マリウス葉", 21)
```

```python
# 間違いの例

# 風磨くんの年齢差は3
("風磨くん", "菊池風磨", 22)
("風磨くん", "菊池風磨", 25)

# でも勝利君の年齢差は2 → 間違いなのでFalseを返す
("勝利くん", "佐藤勝利", 20)
("勝利くん", "佐藤勝利", 22)
```

そこで、`for`ループを使って、順に

1. 今調べているメンバーと、その次のメンバーのふたつの引数間の年齡の差をそれぞれ計算し
2. その差を比較する

という処理を最後のメンバーまで繰り返し行うことにします。

```python
def check_future_age(current_members, future_members):
    for # ???:
        # 今調べているメンバーと次のメンバーの
        # 引数間の年齡の差を比べる
        if # ???:
            # 一人でも違えば`False`を返す
            return False

    # 全員同じであれば`True`を返す
    return True
```

### Step2: `for`ループを書く

`for`ループの中では、「今調べているメンバー」と、「その次のメンバー」の2人分の年齡が必要です。

そこで`range()`を使い、変数`i`には、**「今調べているメンバー」のリスト内の位置**を順に渡せるようにします。

こうすることで、「その次のメンバー」の位置は`i + 1`で表せるようになります。

Se<span class="color-red-600">xy</span> Zoneのようにメンバーが5人の場合、最後に比べるのは4人目のメンバー(`i = 3`)と5人目のメンバー(`i + 1 = 4`)の年齡です。

つまり、`i`には`0`から`3`、すなわち`リストの要素の個数 - 2`までの値を順に代入していけばよいことになります。

`range(a, b)`とすると、`i`には`a`から`b - 1`の数字が入るので、`range(0, len(current_members)-1)`にすれば良さそうです。カウントずれに気をつけましょう!

```python
def check_future_age(current_members, future_members):
    for i in range(0, len(current_members) - 1):
        if # ...
```

これで、調べたい2人のメンバーのリスト内の位置を表すことができるようになりました。

## Step3: `if`の中身を考える

`if`の中身を考えていきます。

年齡はタプルの`[2]`に入っているので、今調べているメンバー、その次のメンバーのふたつの引数間の年齡の差は、それぞれ以下の式で表すことができます。

```python
# 今調べているメンバーの年齡差
current_members[i][2] - future_members[i][2]

# その次のメンバーの年齡差
current_members[i+1][2] - future_members[i+1][2]
```

この2つの年齡差を比較し、同じでない場合は`False`を返したいので、`if`の中には以下のような式を書くことにします。

```python
def check_future_age(current_members, future_members):
    for i in range(0, len(current_members)-1):
        # 2つの年齢差が同じでない場合
        if (current_members[i][2] - future_members[i][2]) != \
           (current_members[i+1][2] - future_members[i+1][2]):
            # `False`を返す
            return False

    return True
```

完成です!🌹🌹

正しい例、間違った例でそれぞれ試してみます。

```python
print(check_future_age(
    [
        ("聡ちゃん", "松島聡", 19),
        ("マリ", "マリウス葉", 17),
        ("ケンティー", "中島健人", 23),
        ("風磨くん", "菊池風磨", 22),
        ("勝利くん", "佐藤勝利", 20)
    ],
    # 正しい3年後の年齡
    [
        ("聡ちゃん", "松島聡", 22),
        ("マリ", "マリウス葉", 20),
        ("ケンティー", "中島健人", 26),
        ("風磨くん", "菊池風磨", 25),
        ("勝利くん", "佐藤勝利", 23)
    ]
))

print(check_future_age(
    [
        ("聡ちゃん", "松島聡", 19),
        ("マリ", "マリウス葉", 17),
        ("ケンティー", "中島健人", 23),
        ("風磨くん", "菊池風磨", 22),
        ("勝利くん", "佐藤勝利", 20)
    ],
    # 間違った3年後の年齡
    [
        ("聡ちゃん", "松島聡", 22),
        ("マリ", "マリウス葉", 20),
        ("ケンティー", "中島健人", 26),
        ("風磨くん", "菊池風磨", 25),
        # ↓正しくは23歳
        ("勝利くん", "佐藤勝利", 22)
    ]
))
```

ちゃんと`True`、`False`と出力されました!

```
❯ python3.6 check_future_age.py
True
False
```

## おわりに


<figure>
    <img src="/images/janiota-python-practice/IMG_0093.jpg" />
    <figcaption>

    </figcaption>
</figure>

以上、初心者向けのPython練習問題5問でした。少しでも世界平和とセクシー時代の構築に貢献できたら幸いです。ご感想は[ツイッター](http://twitter.com/sayajewels)までお寄せください。

最後に、ここまで読んでくださった皆さまは[セクガル・セクボ](http://d.hatena.ne.jp/keyword/%A5%BB%A5%AF%A5%AC%A5%EB)の素質があることに間違いなしです！！！Se<span class="color-red-600">xy</span> Zoneのリア恋枠担当、菊池風磨くん初主演ドラマ[「吾輩の部屋である」](http://www.ntv.co.jp/wagaheya/)月曜深夜24:59〜日本テレビ系にて放送中！！！！！！疲れた夜に見るべし！！！！！！（※もっと疲れるかもしれません。）

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">プログラミング歴ゼロの31歳ジャニヲタ、Pythonを学ぶ。超初心者向けの練習問題を5問紹介。 | Saya’s Blog <a href="https://t.co/WOfYjJ0CVH">https://t.co/WOfYjJ0CVH</a> <a href="https://twitter.com/sayajewels?ref_src=twsrc%5Etfw">@sayajewels</a>さんから</p>&mdash; Saya (@sayajewels) <a href="https://twitter.com/sayajewels/status/923445772418301952?ref_src=twsrc%5Etfw">2017年10月26日</a></blockquote>
