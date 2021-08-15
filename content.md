# 2021.8.18

---

# Question!

--


> Q.バスケットボールの得点は、フリースローが1点、スリーポイントラインの内側からだと2点、外側からだと3点入ります。<br>
> <br>
> ちょうど得点が10点になるまでの得点経過は何通りあるでしょうか？(15秒)

---

<!-- 結論 -->
# Answer!

--

# 274通り

意外と多い

---

<!-- あらすじ -->
たのしいたのしい

# 解法

--

# 考え方

- 10点までのプロセス
    - 9点+フリースロー（1点）
    - 8点+内側(2点)
    - 7点+スリーポイント(3点)

Note:

- この3種類

--

> n点まで何通りか？

<br>

- をf(n)で表すとき
    - 9点+フリースロー（1点）
    - 8点+内側(2点)
    - 7点+スリーポイント(3点)
- これは
    - f(10)=f(9)+f(8)+f(7) <!-- .element: class="fragment" data-fragment-index="1" -->

Note:

- (click) 
- 9点まで、8点まで、7点まで、のそれぞれのいく通りかの総和になる

--

つまり

--

- f(10)=f(9)+f(8)+f(7)
- f(9)=f(8)+f(7)+f(6)
- f(8)=f(7)+f(6)+f(5)
- :
- f(4)=f(3)+f(2)+f(1)

こう表せる

- 式もみえる <!-- .element: class="fragment" data-fragment-index="1" -->
    - `f(n)=f(n-1)+f(n-2)+f(n-3)`

--

f(1),f(2),f(3)は？

Note:

4. 1,2,3は組み合わせを自分で考えると

--

- f(1)=1
    - フリースローの1通り
    - =f(0)+f(-1)+f(-2)<!-- .element: class="fragment" data-fragment-index="1" -->
        - このことからf(0)を1と仮定
- f(2)=2 <!-- .element: class="fragment" data-fragment-index="2" -->
    - フリースローx2、と内側の2通り <!-- .element: class="fragment" data-fragment-index="2" -->
    - =f(1)+f(0)+f(-1) <!-- .element: class="fragment" data-fragment-index="3" -->
    - =1+1+0 <!-- .element: class="fragment" data-fragment-index="4" -->
- f(3)=4 <!-- .element: class="fragment" data-fragment-index="5" -->
    - フリースローx3とスリーポイントと内側+フリースロー（順逆有）の4通り <!-- .element: class="fragment" data-fragment-index="6" -->
    - =f(2)+f(1)+f(0) <!-- .element: class="fragment" data-fragment-index="7" -->
    - =2+1+1 <!-- .element: class="fragment" data-fragment-index="8" -->

--

あとは計算すると

--

f(n) | n
--: | --:
f(0) | 1
f(1) | 1
f(2) | 2
f(3) | 4
f(4) | 7
f(5) | 13
f(6) | 24
f(7) | 44
f(8) | 81
f(9) | 149
<span style="color: green;">f(10)</span> | <span style="color: orange;">274</span>
<!-- .element: style="font-size: 0.7em;" -->

`f(n)=f(n-1)+f(n-2)+f(n-3)` <!-- .element: class="fragment" data-fragment-index="1" -->

--

`f(n)=f(n-1)+f(n-2)+f(n-3)`

似たような式があったような？

Note:

フィボナッチ数列？

--

f(n) | n | n
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
f(10) | 107 | 274
<!-- .element: style="font-size: 0.7em;" -->

Note:

- フィボナッチ数列は、直前2つの合計
- 直前3つの合計は、トリボナッチ数列

--

<!-- 疑問と検証 -->

Q. フィボナッチ数列やトリボナッチ数列の使い道は？
実用的なトリボナッチ数列

---

<!-- まとめ -->

# 数学楽しい
