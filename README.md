## List of Bash operators

This document contains a list of all bash operators 

<table>
  <tr><td width=33% valign=top>

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
  - [-a operator]()
  - [-o operator]()
  - [&& operator]()
  - [|| operator]()
  - [! operator]()
- [ternary operator](#ternary-operator)
- [comma operator](#comma-operator)

</td><td width=33% valign=top>

- [bitwise operators](#bitwise-operators)
  - [& operator]()
  - [| operator]()
  - [^ operator]()
  - [>> operator]()
  - [<< operator]()
  - [~ operator]()
  - [&= operator]()
  - [|= operator]()
  - [^= operator]()
  - [>>= operator]()
  - [<<= operator]()
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

</td><td width=33% valign=top>

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

***

## arithmetic operators

### arithmetic addition operator

The `+` operator is an arithmetic operator used to add numeric values:

```shell
echo $((2 + 2)) # 4

echo `expr 2 + 2` # 4
```

The arithmetic `+` operator can be used as binary operator or as unary operator:

```shell
echo $((+ 2)) # 2
```

NB:

The `expr` program is deprecated, because it is pre-POSIX, please avoid using it.

### arithmetic subtraction operator

The `-` operator is an arithmetic operator used to subtraction numeric values:

```shell
echo $((3 - 2)) # 1
```

The arithmetic `-` operator can be used as binary operator or as unary operator:

```shell
echo $((- 2)) # -2


echo $((- -5)) # 5
```

### arithmetic multiplication operator

The `*` operator is an arithmetic operator used to multiply numeric values:

```shell
echo $((3 * 2)) # 6
```

### arithmetic division operator

The `/` operator is an arithmetic operator used to divide numeric values:

```shell
echo $((3 / 2))     # 1
echo $((3.0 / 2))   # 1.5
echo $((3 / 2.0))   # 1.5
```

### arithmetic module operator

The `%` operator is an arithmetic operator used to get the rest of the division:

```shell
echo $((5 % 2.4))   # 0.2
```

### arithmetic power operator

The `**` operator is an arithmetic operator used to obtain the result of elevation to power:

```shell
echo $(( 2 ** 3))   # 8
```

### arithmetic increment operator

The `++` operator is used to increment the value of a variable by 1.
When the operator is used before the variable then it will 
act as a pre-increment operator that means the value of the variable 
will be incremented first and will do other operation later.

```shell
i=9

echo $((++ i + 10)) # 10
```

When the `++` operator is used after the variable then it will act as post-increment 
operator, and it will increment the value of the variable by 1 after doing another task.

```shell
i=9

echo $((i ++))    # 9
echo $((i))       # 10
```

### arithmetic decrement operator

The `--` operator is the same as the `++` operator, except it decrements the value of the variable by 1.

```shell
i=10
echo $((--i))     # 9
echo $((i--))     # 9
echo $((i))       # 8
```

### arithmetic addition assign operator

The `+=` operator is a shortcut for `a = a + x`

### arithmetic subtraction assign operator

The `-=` operator is a shortcut for `a = a - x`

### arithmetic multiplication assign operator

The `*=` operator is a shortcut for `a = a * x`

### arithmetic division assign operator

The `/=` operator is a shortcut for `a = a / x`

### arithmetic module assign operator

The `%=` operator is a shortcut for `a = a % x`

### arithmetic power assign operator

The `**=` operator is a shortcut for `a = a ** x`

## Logical operators

## Ternary operator

## Comma operator

## Bitwise operators

## Comparison operators

## String operators

## File operators

## Redirect operators
