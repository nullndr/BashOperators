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
  - [+= operator]()
  - [-= operator]()
  - [*= operator]()
  - [/= operator]()
  - [%= operator]()
  - [**= operator]()
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

echo `expr + 2` # 2
```

### arithmetic subtraction operator

The `-` operator is an arithmetic operator used to subtraction numeric values:

```shell
echo $((3 - 2)) # 1

echo `expr 3 - 2` # 1
```

The arithmetic `-` operator can be used as binary operator or as unary operator:

```shell
echo $((- 2)) # -2


echo $((- -5)) # 5
```

### arithmetic multiplication operator

### arithmetic division operator

### arithmetic module operator

### arithmetic power operator

### arithmetic increment operator

### arithmetic decrement operator

## Logical operators

## Ternary operator

## Comma operator

## Bitwise operators

## Comparison operators

## String operators

## File operators

## Redirect operators
