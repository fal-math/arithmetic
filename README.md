# atirhmetic

## ゆくゆくやりたいこと

LaTeX 形式で入力 → 字句解析 → 計算 → LaTeX 形式で出力

## 計算例

- x^2 y z + x y
  - Add(Times(Times(Unary(x, 2, 1), Unary(y, 1, 1)), Unary(z, 1, 1)), Times((Unary(x, 1, 1), Unary(y, 1, 1))) )

- x/y - y/x
  - Sub(Times(Unary(x, 1, 1), Unary(y, -1, 1)), Times(Unary(y, 1, 1), Unary(x, -1, 1)))

## data型

- Exp 型
  - Unary
  - UOpExp

- Unary 型
  - (string, int, int) (文字,分子,分母)

- Oper 型
  - Plus
  - Minus
  - Times
  - Div