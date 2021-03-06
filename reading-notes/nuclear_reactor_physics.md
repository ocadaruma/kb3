https://rpg.jaea.go.jp/else/rpd/others/study/text_aesj.html

## 1. 原子核の物理

#### 例題1.1
- 重水素原子の原子量を2.01410u, 水素原子の原子量を1.00783uとした時、重水素の質量欠損を求めよ

```
- A: 質量数（陽子の数 + 中性子の数）
- Z: 原子番号（陽子の数）
- Mp: 陽子の質量
- Mn: 中性子の質量
- M(A, Z): 質量数A、原子番号Zの原子核の質量

としたとき、質量欠損ΔMは以下で計算される。

ΔM = ZMp + (A - Z)Mn - M(A, Z)

重水素はA=1, Z=1なので
ΔM = Mp + Mn - M(1, 1)

ここで電子の質量をMeとして式を変形すると
ΔM = Mp + Me + Mn - (M(1, 1) + Me)

質量欠損は結合エネルギーのために原子核の質量が核子の質量の総和より小さくなる現象である。
したがって、原子核が陽子一つのみからなる水素においては質量欠損が存在せず（本当？）Mp + Meは単純に原子の質量と一致する。

また、M(1, 1) + Meは重水素原子の質量にほかならない。合わせると、

ΔM = 1.00783 + 1.00866 (中性子の質量) - 2.01410 = 0.00239
```

#### 例題1.2

式にしたがって真面目に計算してもいいが、水素のK電子の結合エネルギーが13.60eVと与えられているため、これを使った方が簡単。

```
式のZ以外の係数をCとおくと、原子番号Zの原子におけるK電子の結合エネルギーは
Ez = C * Z^2

水素のK電子の結合エネルギーが13.60eV、鉛の原子番号はZ=82であることから、
E82 = 82^2 * 13.60eV
    = 91.4464 KeV
```

#### 例題1.3

N(t)を時刻tにおける放射性核種の個数、崩壊定数をλとすると、

```
dN(t)/dt = -λN(t) という微分方程式に従うのだった。

これは定数係数微分方程式であり、一般解は
N(t) = Ce^-λt
で与えられる。t = 0を代入してみればC = N(0)であるから、結局
N(t) = N(0)e^-λt
となる。

半減期Tとは、N(T)がN(0)の1/2になる時刻Tのことをいう。
つまり

N(0)/2 = N(0)e^-λT

をTについて解けばよい。

N(0)/2 = N(0)e^-λT
1/2 = e^-λT
1 = 2e^-λT

ln(1) = ln(2e^-λT)
0 = ln(2) - λT
T = ln(2) / λ
  = 0.693 / λ
```

#### 例題1.4

```
親核種が7Be、娘核種が7Liのとき、中性原子の質量差は
7.01693 - 7.01600 = 0.00093u
である。
1u = 931.49MeV
であったので、これは931.49 * 0.00093 = 0.8662857Mevにあたる。

これは電子質量の2倍1.02MeVより小さいため、β+崩壊は起きず、軌道電子捕獲のみが起きる。
```

#### 例題1.5

```
Q = (M_A + Ma - (M_B + Mb)) * c^2

ここで、cは光速である。
捕獲反応 157Gd + n -> 158Gd + γ では
M_A = 156.924u
Ma = 1.00866u
M_B = 157.924u
放出粒子は無いので Mb = 0

である。
Q値の計算式に従うと、
Q = ((156.924 + 1.00866) - 157.924) * c^2
  = 0.00866u * c^2

1u * c^2 = 931.49MeVであったことを思い出すと、
Q = 0.00866 * 931.49MeV = 8.0667MeV
```

#### 例題1.6

```
ふたたびQ値の計算式にしたがうと（というかQ値は単に反応前後の静止エネルギーの差分である）

Q = (235.044 + 1.00866 - (146.928 + 86.921 + 2 * 1.00866)) * c^2
  = 0.18634 * c^2
  = 173.57MeV
```

#### 例題1.7

単に反応前後の静止エネルギーの差分を求める。
```
Q = ((2.01410 + 3.01605) - (4.00260 + 1.00866)) * c^2
  = 0.01889 * c^2
  = 17.596MeV
```

## 2. 中性子と物質の反応

#### 例題2.1

反応率の計算式にしたがい計算するだけ。
```
R = 2.5 * 10^-28 * 2.0 * 10^16 * 8.0 * 10^27
  = 2.5 * 2.0 * 8.0 * 10^15
  = 4.0 * 10^16
```

#### 例題2.2

原子炉の振る舞いを考える際には`σ_a`は実質的に`σ_f + σ_c`となる事実より、
```
σ_a = σ_f + σ_c
    = 500 + 150
    = 650b

および

σ_t = σ_a + σ_s
    = 650 + 10
    = 660b
```

核分裂反応が起こる確率（問題の表現が分かりにくいが、「核反応全体に対し何%の確率で核分裂が起きるか」という意味合いのようだ）は
```
σ_f / σ_t = 500 / 660 
          = 75.76%
```
