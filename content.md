# 2021.8.25

Note:

まずは..

---

# Question!

Note:

こちらを

--


<!-- .slide: style="background-color:rgba(0,0,0,0.5); " -->
<!-- .slide: data-background-image="https://slamdunk-movie.jp/assets/img/main01.png" data-background-size="50%" -->

### Q. バスケットボールの得点は、フリースローが<span style="color: blue;">1</span>点、スリーポイントラインの外側からだと<span style="color: lime;">3</span>点、内側からだと<span style="color: yellow;">2</span>点入ります。

### ちょうど得点が<span style="color: orange;">10</span>点になるまでの得点経過は何通りあるでしょうか？(15秒)

Note:

- Q. バスケットボールの得点は、フリースローが<span style="color: blue;">1</span>点、スリーポイントラインの外側からだと<span style="color: lime;">3</span>点、内側からだと<span style="color: yellow;">2</span>点入ります。ちょうど得点が<span style="color: orange;">10</span>点になるまでの得点経過は何通りあるでしょうか？
- はい、いまから15秒

---

<!-- .slide: style="background-color:rgba(0,0,0,0.5); " -->
<!-- .slide: data-background-image="https://slamdunk-movie.jp/assets/img/main01.png" data-background-size="50%" -->

<!-- 結論 -->
# Answer!

Note:

IQ Engine風がよい

--

<!-- .slide: style="background-color:rgba(0,0,0,0.5); " -->
<!-- .slide: data-background-image="https://slamdunk-movie.jp/assets/img/main01.png" data-background-size="50%" -->

# 274通り

Note:

274通り。意外と多い

---

<!-- .slide: style="background-color:rgba(0,0,0,0.5); " -->
<!-- .slide: data-background-image="https://tk.ismcdn.jp/mwimgs/7/f/1140/img_7feca35cadceba79b9b9c0065b3b7dd8399610.jpg" data-background-size="90%" -->

<!-- あらすじ -->
たのしいたのしい

# 解法

Note:


--

<!-- .slide: style="background-color:rgba(0,0,0,0.5); " -->
<!-- .slide: data-background-image="https://tk.ismcdn.jp/mwimgs/7/f/1140/img_7feca35cadceba79b9b9c0065b3b7dd8399610.jpg" data-background-size="90%" -->

# 総当たり！

Note:

- が簡単
- 274通りは日が暮れる...
- 論理的にいく

--

<!-- .slide: style="background-color:rgba(0,0,0,0.5); " -->
<!-- .slide: data-background-image="https://tk.ismcdn.jp/mwimgs/7/f/1140/img_7feca35cadceba79b9b9c0065b3b7dd8399610.jpg" data-background-size="90%" -->

# 考え方

- 10点に至るには？ <!-- .element: class="fragment" data-fragment-index="1" -->
    - 9点から <span style="color: blue;">1</span>点取る（フリースロー）
    - 8点から <span style="color: yellow;">2</span>点取る（スリーポイント内側）
    - 7点から <span style="color: lime;">3</span>点取る（スリーポイント）

Note:

- まず「考え方」
- (click)
- この3種類

--

<!-- .slide: style="background-color:rgba(0,0,0,0.5); " -->
<!-- .slide: data-background-image="https://tk.ismcdn.jp/mwimgs/7/f/1140/img_7feca35cadceba79b9b9c0065b3b7dd8399610.jpg" data-background-size="90%" -->

> n点まで何通りか？

<br>

- をf(n)で表すとき <!-- .element: class="fragment" data-fragment-index="1" -->
- f(10)=<!-- .element: class="fragment" data-fragment-index="1" --><span>f(9)+f(8)+f(7)</span> <!-- .element: class="fragment" data-fragment-index="2" -->

Note:

- n点まで何通りか？
- (click) 
- をf(n)で...f(10)=
- (click) 
- 9点まで、8点まで、7点まで、のそれぞれのいく通りかの総和になる

--

<!-- .slide: style="background-color:rgba(0,0,0,0.5); " -->
<!-- .slide: data-background-image="https://tk.ismcdn.jp/mwimgs/7/f/1140/img_7feca35cadceba79b9b9c0065b3b7dd8399610.jpg" data-background-size="90%" -->

つまり

--

<!-- .slide: style="background-color:rgba(0,0,0,0.5); " -->
<!-- .slide: data-background-image="https://tk.ismcdn.jp/mwimgs/7/f/1140/img_7feca35cadceba79b9b9c0065b3b7dd8399610.jpg" data-background-size="90%" -->

> n点まで何通りか？

<br>

- f(10)=f(9)+f(8)+f(7)
- f(9)=f(8)+f(7)+f(6)
- f(8)=f(7)+f(6)+f(5)
- :
- f(4)=f(3)+f(2)+f(1)

こう表せる

- 式もみえる <!-- .element: class="fragment" data-fragment-index="1" -->
    - `f(n)=f(n-1)+f(n-2)+f(n-3)`

Note:

- n点まで何通りか？
- こう表せる
- (click) 
- 式も見える（詳細は後で）

--

<!-- .slide: style="background-color:rgba(0,0,0,0.5); " -->
<!-- .slide: data-background-image="https://tk.ismcdn.jp/mwimgs/7/f/1140/img_7feca35cadceba79b9b9c0065b3b7dd8399610.jpg" data-background-size="90%" -->

f(1),f(2),f(3)は？

Note:

4. 1,2,3は組み合わせを自分で総当たりで考えると

--

<!-- .slide: style="background-color:rgba(0,0,0,0.5); font-size: 0.7em;" -->
<!-- .slide: data-background-image="https://tk.ismcdn.jp/mwimgs/7/f/1140/img_7feca35cadceba79b9b9c0065b3b7dd8399610.jpg" data-background-size="90%" -->

> f(1),f(2),f(3)は？

- f(1)=1
    - フリースローの1通り
    - =f(0)+f(-1)+f(-2)<!-- .element: class="fragment" data-fragment-index="1" -->
        - このことからf(0)を1と仮定（n<0はちょっと...）
- f(2)=2 <!-- .element: class="fragment" data-fragment-index="2" -->
    - フリースローx2、と内側の2通り <!-- .element: class="fragment" data-fragment-index="2" -->
    - =f(1)+f(0)+f(-1) <!-- .element: class="fragment" data-fragment-index="3" -->
    - =1+1+0 =2 <!-- .element: class="fragment" data-fragment-index="4" -->
- f(3)=4 <!-- .element: class="fragment" data-fragment-index="5" -->
    - フリースローx3とスリーポイントと内側+フリースロー（順逆有）の4通り <!-- .element: class="fragment" data-fragment-index="5" -->
    - =f(2)+f(1)+f(0) <!-- .element: class="fragment" data-fragment-index="6" -->
    - =2+1+1 =4 <!-- .element: class="fragment" data-fragment-index="7" -->

Note:

- f(1)は、フリースローの1通り
- (click)
- 公式に当てると、f(0)+f(-1)+f(-2) になるが、f(0)が1でしょう
- (click)
- f(2)は、フリースローと2点の2通り
- (click)
- 公式に当てると、f(1)+f(0)+f(-1) になるが、(click) f(0)とf(1)は1だから2になる。公式も合ってる
- (click)
- f(3)は、フリースローと2点とスリーポイントの4通り
- (click)
- 公式に当てると、f(2)+f(1)+f(0) になるが、(click) 4になる。公式も合ってる

--

<!-- .slide: style="background-color:rgba(0,0,0,0.5); " -->
<!-- .slide: data-background-image="https://tk.ismcdn.jp/mwimgs/7/f/1140/img_7feca35cadceba79b9b9c0065b3b7dd8399610.jpg" data-background-size="90%" -->

あとは計算すると

Note:

- あとは計算する。単純な足し算

--

<!-- .slide: style="background-color:rgba(0,0,0,0.5); " -->
<!-- .slide: data-background-image="https://tk.ismcdn.jp/mwimgs/7/f/1140/img_7feca35cadceba79b9b9c0065b3b7dd8399610.jpg" data-background-size="90%" -->

f(n) | | n
--: | --- | --:
f(0) | | 1
f(1) | =f(0) | 1
f(2) | =f(1)+f(0) | 2
f(3) | =f(2)+f(1)+f(0) | 4
f(4) | =f(3)+f(2)+f(1) | 7
f(5) | =f(4)+f(3)+f(2) | 13
f(6) | =f(5)+f(4)+f(3) | 24
f(7) | =f(6)+f(5)+f(4) | 44
f(8) | =f(7)+f(6)+f(5) | 81
f(9) | =f(8)+f(7)+f(6) | 149
<span style="color: lime;">f(10)</span> | =f(9)+f(8)+f(7) | <span style="color: orange;">274</span>
<!-- .element: style="font-size: 0.7em;" -->

Note:

- 足し算、f(4)は7, f(5)は13と続けるとf(10)は274

--

<!-- .slide: style="background-color:rgba(0,0,0,0.5); " -->
<!-- .slide: data-background-image="https://tk.ismcdn.jp/mwimgs/7/f/1140/img_7feca35cadceba79b9b9c0065b3b7dd8399610.jpg" data-background-size="90%" -->

`f(n)=f(n-1)+f(n-2)+f(n-3)`

似たような式があったような？

Note:

- さてこの数式、似たようなものを観た気が？
- フィボナッチ数列？

--

<!-- .slide: style="background-color:rgba(0,0,0,0.5); " -->
<!-- .slide: data-background-image="https://tk.ismcdn.jp/mwimgs/7/f/1140/img_7feca35cadceba79b9b9c0065b3b7dd8399610.jpg" data-background-size="90%" -->

f(n) | フィボナッチ<br>数列 | トリボナッチ<br>数列
--: | --: | --:
f(0) | 1 | 1
f(1) | 1 | 1
f(2) | 2 | 2
f(3) | 3 | 4
f(4) | 5 | 7
f(5) | 8 | 13
f(6) | 13 | 24
f(7) | 21 | 44
f(8) | 44 | 81
f(9) | 63 | 149
f(10) | 107 | <span style="color: orange;">274</span>
<!-- .element: style="font-size: 0.7em;" -->

Note:

- フィボナッチ数列は、直前2つの合計
- 直前3つの合計は、トリボナッチ数列
- 今回のバスケ問題は、トリボナッチ数列で解決
- なんとも不思議な感覚

--

<!-- 疑問と検証 -->

<!-- .slide: style="background-color:rgba(0,0,0,0.5); " -->
<!-- .slide: data-background-image="https://tk.ismcdn.jp/mwimgs/7/f/1140/img_7feca35cadceba79b9b9c0065b3b7dd8399610.jpg" data-background-size="90%" -->

Q. フィボナッチ数列や<br>トリボナッチ数列の使い道は？

Note:

- 使い道なんかあるんかい？

--

<!-- .slide: style="background-color:rgba(255,255,255,1); " -->

<img class="r-stretch" src="https://static.wixstatic.com/media/0adbae_e6d1359168e1423ea7023399b372c620~mv2.png" >

Note:

- ありました。というか
- フィボナッチ数列は自然界に存在してる
- まつぼっくり、螺旋模様。右回りで数えた時と左回りで数えた時に、隣り合ったフィボナッチ数列が見える
- キク科の花の螺旋も、パイナップルの皮の螺旋も。
- 種の保存に適した数列っぽいが、全容解明はされてない

---

<!-- まとめ -->

<!-- .slide: style="background-color:rgba(0,0,0,0.5); " -->
<!-- .slide: data-background-image="https://tk.ismcdn.jp/mwimgs/7/f/1140/img_7feca35cadceba79b9b9c0065b3b7dd8399610.jpg" data-background-size="90%" -->

# 数学楽しい

Note:


