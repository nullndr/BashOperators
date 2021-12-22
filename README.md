## List of Bash operators

This document contains a list of all bash operators with their description.

<table>
  <tr><td width=33% valign="top">

- [arithmetic expansion](#arithmetic-expansion)
- [arithmetic operators](#arithmetic-operators)
  - [+ operator](#arithmetic-addition-operator)
  - [- operator](#arithmetic-subtraction-operator)
  - [* operator](#arithmetic-multiplication-operator)
  - [/ operator](#arithmetic-division-operator)
  - [% operator](#arithmetic-module-operator)
  - [** operator](#arithmetic-power-operator)
  - [++ operator](#arithmetic-increment-operator)
  - [-- operator](#arithmetic-decrement-operator)
  - [+= operator](#arithmetic-addition-assign-operator)
  - [-= operator](#arithmetic-subtraction-assign-operator)
  - [*= operator](#arithmetic-multiplication-assign-operator)
  - [/= operator](#arithmetic-division-assign-operator)
  - [%= operator](#arithmetic-module-assign-operator)
  - [**= operator](#arithmetic-power-assign-operator)
- [logical operators](#logical-operators)
  - [&& operator](#logical-and-operator)
  - [|| operator](#logical-or-operator)
  - [! operator](#logical-not-operator)
- [ternary operator](#ternary-operator)
- [comma operator](#comma-operator)

</td><td width=33% valign="top">

- [bitwise operators](#bitwise-operators)
  - [& operator](#bitwise-and-operator)
  - [| operator](#bitwise-or-operator)
  - [^ operator](#bitwise-xor-operator)
  - [~ operator](#bitwise-not-operator)
  - [>> operator](#bitwise-rightshift-operator)
  - [<< operator](#bitwise-leftshift-operator)
  - [&= operator](#bitwise-and-assign-operator)
  - [|= operator](#bitwise-or-assign-operator)
  - [^= operator](#bitwise-xor-assign-operator)
  - [>>= operator](#bitwise-rightshift-assign-operator)
  - [<<= operator](#bitwise-leftshift-assign-operator)
- [comparison operators](#comparison-operators)
  - [-eq operator]()
  - [-ne operator]()
  - [-gt operator]()
  - [-ge operator]()
  - [-lt operator]()
  - [-le operator]()
  - [> operator]()
  - [>= operator]()
  - [< operator]()
  - [<= operator]()
- [string operators](#string-operators)
  - [-z operator]()
  - [-n operator]()
  - [= operator]()
  - [== operator]()
  - [!= operator]()
  - [< operator]()
  - [> operator]()

</td><td width=33% valign="top">

- [file operators](#file-operators)
  - [-b operator]()
  - [-c operator]()
  - [-d operator]()
  - [-e operator]()
  - [-f operator]()
  - [-g operator]()
  - [-h operator]()
  - [-k operator]()
  - [-p operator]()
  - [-r operator]()
  - [-s operator]()
  - [-t operator]()
  - [-u operator]()
  - [-w operator]()
  - [-x operator]()
  - [-ef operator]()
  - [-nt operator]()
  - [-ot operator]()
  - [-G operator]()
  - [-N operator]()
  - [-O operator]()
  - [-S operator]()
- [redirect operators](#redirect-operators)
  - [> operator]()
  - [>> operator]()
  - [< operator]()
    </td>
  </tr>
</table>

---

<a id="arithmetic-expansion"></a>
## arithmetic expansion

The `$(( ... ))` is known as arithmetic expansion, which is evaluated and expands to the result.

The output is guaranteed to be one word and a digit in Bash.

The oldest form, `$[ ... ]` is deprecated and must not be used; also, 
the `expr` program is deprecated, because it is pre-POSIX, please avoid using it.

---

<a id="arithmetic-operators"></a>
## arithmetic operators

The arithmetic operators are used to perform basic arithmetic operations.

<a id="arithmetic-addition-operator"></a>
### + operator

The `+` operator is an arithmetic operator used to add numeric values:

```shell
$ echo $((2 + 2))
4
```

The arithmetic `+` operator can be used as binary operator or as unary operator:

```shell
$ echo $((+ 2))
2
```

<a id="arithmetic-subtraction-operator"></a>
### - operator

The `-` operator is an arithmetic operator used to subtraction numeric values:

```shell
$ echo $((3 - 2)) 
1
```

The arithmetic `-` operator can be used as binary operator or as unary operator:

```shell
$ echo $((- 2))
-2

$ echo $((- -5)) 
5
```

<a id="arithmetic-multiplication-operator"></a>
### * operator

The `*` operator is an arithmetic operator used to multiply numeric values:

```shell
$ echo $((3 * 2))
6
```

<a id="arithmetic-division-operator"></a>
### / operator

The `/` operator is an arithmetic operator used to divide numeric values:

```shell
$ echo $((3 / 2))
1

$ echo $((3.0 / 2))
1.5

$ echo $((3 / 2.0)) 
1.5
```

<a id="arithmetic-module-operator"></a>
### % operator

The `%` operator is an arithmetic operator used to get the rest of the division:

```shell
$ echo $((5 % 2.4))
0.2
```

<a id="arithmetic-power-operator"></a>
### ** operator

The `**` operator is an arithmetic operator used to obtain the result of elevation to power:

```shell
$ echo $(( 2 ** 3))
8
```

<a id="arithmetic-increment-operator"></a>
### arithmetic increment operator

The `++` operator is used to increment the value of a variable by 1.
When the operator is used before the variable then it will 
act as a pre-increment operator that means the value of the variable 
will be incremented first and will do other operation later.

```shell
$ i=9

$ echo $((++ i + 10))
20
```

When the `++` operator is used after the variable then it will act as post-increment 
operator, and it will increment the value of the variable by 1 after doing another task.

```shell
$ i=9

$ echo $((i ++))
9

$ echo $((i))
10
```

<a id="arithmetic-decrement-operator"></a>
### arithmetic decrement operator

The `--` operator is the same as the `++` operator, except it decrements the value of the variable by 1.

```shell
$ i=10

$ echo $((--i))
9

$ echo $((i--))
9

$ echo $((i))
8
```

<a id="arithmetic-addition-assign-operator"></a>
### arithmetic addition assign operator

The `+=` operator is a shortcut for `a = a + x`.

```bash
$ a=10

$ echo $((a += 10))
20

$ echo $a
20
```

<a id="arithmetic-subtraction-assign-operator"></a>
### arithmetic subtraction assign operator

The `-=` operator is a shortcut for `a = a - x`.

<a id="arithmetic-mmultiplication-assign-operator"></a>
### arithmetic multiplication assign operator

The `*=` operator is a shortcut for `a = a * x`.

<a id="arithmetic-division-operator"></a>
### arithmetic division assign operator

The `/=` operator is a shortcut for `a = a / x`.

<a id="arithmetic-module-assign-operator"></a>
### arithmetic module assign operator

The `%=` operator is a shortcut for `a = a % x`.

<a id="arithmetic-power-assign-operator"></a>
### arithmetic power assign operator

The `**=` operator is a shortcut for `a = a ** x`.

---

<a id="logical-operators"></a>
## Logical operators

The logical operators are used to perform logical operations.

<a id="logical-and-operator"></a>
### && logical operator

The `&&` operator is a comparison operator that is used to create the boolean AND logic.

When all conditions are true, then the AND gate return true

```bash
$ echo true && true

$ echo $?
0

$ echo false && false

$ echo $?
1

$ echo true && false

$ echo $?
1

$ echo false && true

$ echo $?
1
```

The `&&` operator is known as short-circuit operator, enabling you
to not evaluating the right side of the expression when the overall
result of the expression can be predicted from the left side value.

Let me show you a simple example:

```bash
$ true && echo "Hello"
Hello
```

This is simple, the left side (`true`) is evaluated as true, then the
right side can be evaluated, displaying `Hello`.

But check this:

```bash
$ false && echo "Hello"
```

Nothing is displayed, this because the left side is evaluated as false,
so the `&&` obviously will return false, so there is no need to evaluate
the right side.

<a id="logical-or-operator"></a>
### || logical operator

The `||` operator is a comparison operator that is used to create the boolean OR logic.

When one or all conditions are true, then the OR gate return true

```bash
$ echo true && true

$ echo $?
0

$ echo false && false

$ echo $?
1

$ echo true && false

$ echo $?
0

$ echo false && true

$ echo $?
0
```

The `||` operator is known as short-circuit operator, enabling you
to not evaluating the right side of the expression when the overall
result of the expression can be predicted from the left side value.

Let me show you a simple example:

```bash
$ false || echo "Hello"
Hello
```

This is simple, the left side (`false`) is evaluated as false, then the
right side is evaluated, displaying `Hello`.

But check this:

```bash
$ true || echo "Hello"
```

Nothing is displayed, this because the left side is evaluated as true,
so the `||` obviously will return true, so there is no need to evaluate
the right side.

<a id="logical-not-operator"></a>
### ! logical operator

The `!` operator transform a `true` into a `false` and vice-versa.

---

## Ternary operator

---

## Comma operator

---

<a id="bitwise-operators"></a>
## Bitwise operators

The bitwise operators are operators used to perform bit operations on pattern.

<a id="bitwise-and-operator"></a>
### & operator

The `&` operator perform the bitwise AND gate.

```bash
$ echo $((4 & 3))
0
```

The AND will be executed on each bit of each expression:

```
4 -> 100
3 -> 011
& -> 000
```

<a id="bitwise-or-operator"></a>
### | operator

The `|` operator perform the bitwise OR gate.

```bash
$ echo $((4 & 3))
7
```

The OR will be executed on each bit of each expression:

```
4 -> 100
3 -> 011
| -> 111
```

<a id="bitwise-xor-operator"></a>
### ^ operator

The `^` perform the bitwise eXclusive OR (XOR) gate.

```bash
$ echo $((5 ^ 3))
6
```

The XOR will be executed on each bit of each expression:

```
5 -> 101
3 -> 011
^ -> 110
```

<a id="bitwise-not-operator"></a>
### ~ operator

The `~` operator perform the bitwise negation.

```bash
echo $((~ 8))
-9
```

The `~` is performed on each bit of the expression.

```
8 -> 1000
~ -> 0111
```

<a id="bitwise-rightshift-operator"></a>
### >> operator

The `>>` operator perform the right shift of the expression.

<a id="bitwise-leftshift-operator"></a>
### << operator

The `<<` operator is used to perform the left shift of the expression.

<a id="bitwise-and-assign-operator"></a>
### &= operator

<a id="bitwise-and-assign-operator"></a>
### |= operator

<a id="bitwise-and-assign-operator"></a>
### ^= operator

<a id="bitwise-rightshift-assign-operator"></a>
### >>= operator

<a id="bitwise-leftshift-assign-operator"></a>
### <<= operator

## Comparison operators

---

## String operators

---

## File operators

---

## Redirect operators

---