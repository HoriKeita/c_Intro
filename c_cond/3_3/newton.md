# 応用問題

1. $\sqrt{2}$の数列1.414214を導出するプログラムを作成せよ。ただし、math.hなどのライブラリは使用してはならない。

## ヒント

問題を$\mathbb{R}\rightarrow \mathbb{R}, x \in \mathbb{R}$として
$$ f(x)=0 $$
となる$x$を求めることを考える。
このとき、適当な値$x_0$をとり、次の漸化式により、xに収束する数列を得ることができる。
$$ x_{n+1}=x_n-\frac{f(x_n)}{f'(x_n)} $$
ここで、$\sqrt{2}$を求める場合は
$$ f(x)=x^2-2 $$
とおき、$f(x)=0$の解を求める問題として解くことができる。

```c
#include <stdio.h>

#define ME 1.0e-6   // 許容誤差
#define absdif(x,y) ((x>y) ? (x-y) : (y-x)) // 差分絶対値

int main(){
    double x = 1.0; // 初期値
    double e = absdif(x + 2/x); // 誤差

    while(e > ME){
        // ここに追記
    }

    print("%f\n",x)
}
```
