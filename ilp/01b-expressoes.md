---
layout: remark
title: Expressões aritméticas em Python
---

{::nomarkdown}
template: inverse

# Expressões aritméticas

{% include_relative footer.txt %}

---

# Expressões aritméticas

Expressões aritméticas podem ser:

- um número. Ex.: `3.2`
- uma variável numérica. Ex.: `x`
- uma operação aritmética envolvendo duas expressões aritméticas. Ex.:
  - `3.2 + x`
  - `(3.2 + x) / 2`
- a aplicação de uma função a uma expressão aritmética. Ex.: `int(3.2 + x)`

---

# Operações aritméticas em Python

| Símbolo |   significado    |
|---------|------------------|
| `+`     | soma             |
| `-`     | subtração        |
| `*`     | multiplicação    |
| `/`     | divisão          |
| `//`    | divisão inteira\*|
| `%`     | resto da divisão |
| `**`    | potenciação      |

\* A **divisão inteira** retorna apenas a parte inteira do resultado. Exemplos:

- Divisão normal: `10 / 4` ==> `2.5`
- Divisão inteira: `10 // 4` ==> `2`

---

# Precedência de operadores

Certas operações possuem maior **precedência**, isto é, são realizadas primeiro. Por exemplo, na expressão `1 + 4 * 3`, a operação de multiplicação (`4 * 3`) é realizada antes da soma.

--

Níveis de precedência de operadores:

- `**` (maior precedência)
- `*`, `/`, `//`, `%`
- `+`, `-` (menor precedência)
- Duas operações no mesmo nível: executar da esquerda para a direita


--


Exemplos:

- `1 + 2 * 3` = ?
- `6 * 6 / 12` = ?
- `4 / 2 * 3` = ?

- Na dúvida, use parênteses para forçar uma precedência. Ex.: `(1 + 2) * 3`

---

# Funções matemáticas

Para usar as [funções matemáticas](https://docs.python.org/3/library/math.html), você precisa incluir a seguinte linha no início de seu código:

```python
from math import *
```

- Funções trigonométricas: `sin(x)`, `cos(x)`, `tan(x)`. Ex.: `cos(3.14)` (note que o valor passado deve estar em radianos)
- Valor absoluto: `fabs(x)`. Ex.: `fabs(-11)` ==> `11`
- Raiz quadrada: `sqrt(x)`. Ex.: `sqrt(9)` ==> `3`.
- Logaritmos: `log(x)` (logaritmo natural, base e), `log10(x)` (base 10)
- Arredondamento: `ceil(x)` (arredonda pra cima), `floor(x)` (arredonda pra baixo)
- Constantes: `pi`, `e`

---
template: exercise
# Exercícios

- Crie um programa para calcular as raízes de uma equação do segundo grau
- Como determinar se um número é par?
- Como extrair o dígito das unidades de um número?
- Como extrair o dígito das dezenas de um número?

---

# Expressões com strings

- Strings admitem a operação de **concatenação**, com o operador `+`
- Exemplo:

```python
nome = "Fulano"
sobrenome = "de Tal"
nome_completo = nome + " " + sobrenome  #=> "Fulano de Tal"
```

{:/}
