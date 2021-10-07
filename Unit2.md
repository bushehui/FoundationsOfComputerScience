# An Introduction to Computer Science <br> (Foundations of Computer Science) <br> 计算机科学导论

---

# Unit 2 <br> Number Systems and Conversions <br> 第二章 <br> 计数系统和转换

---

# Objectives

## You are supposed to be able to :

- <mark>**Understand the basic concepts about a number system.**</mark>
- <mark>**Calculate the value of a number from a specified positional number system. **</mark>
- **Understand the difference between positional system and non-positional System**
- **<mark>Convert a number  between different number systems.</mark>**
- Calculate the value of a Roman Numeral. 

---

# Basic Concept : Number

## <mark>A number is a mathematical object used to count, measure, and label. </mark>

- Calculations with numbers are done with arithmetical operations, the most familiar being addition, subtraction, multiplication, division, and exponentiation. 
- Their study or usage is called arithmetic, a term which may also refer to number theory, the study of the properties of numbers.

## Categories

|Type || Symbol|| |
|:---|:---|:---:|:---|:---|
|Natural (自然数) | | $\mathbb{N}$| | $\mathbb{N}\_{0} = \{ 0, 1, 2, 3, 4, 5, \ldots \}$ or $\mathbb{N}\_{1} = \{ 1, 2, 3, 4, 5, \ldots \}$. |
|Integer (整数) | | $\mathbb{Z}$ | | $\ldots$, $−5$, $−4$, $−3$, $−2$, $−1$, $0$, $1$, $2$, $3$, $4$, $5$, $\ldots$|
|Rational (有理数) | | $\mathbb{Q}$ | | $\frac{a}{b}$, where $a$ and $b$ are integers and $b \neq 0$|
|Real (实数) | | $\mathbb{R}$ | | The limit of a convergent sequence of **rational numbers**|
|Complex (复数) | | $\mathbb{C}$ | | $a + bi$, where $a$ and $b$ are **real numbers** and $i$ is a formal square root of $−1$|

<!---
Main number systems
In mathematics, the notion of a number has been extended over the centuries to include $0$, negative numbers, rational numbers, real numbers, and complex numbers.
--->

<img src="figs/NumberSetinC.png" alt="NumberSetinC" width="150">

<https://en.wikipedia.org/wiki/Number>

---

# Basic Concept : Number System

## <mark> A number system is a series of rules about how a number of specific value can be represented using various symbols. </mark>

- For example :
    - $(2A)\_{16} = (42)\_{10}$
    - $(52)\_8    = (42)\_{10}$

## Two groups of number systems: 
- positional number system (__按位计数系统__)
- non-positional number systems (__非按位计数系统__)

---

# Positional Number System

## Example

$$(150.2)\_{10}$$
$$\Downarrow$$
$$ 1 \times 100 + 5 \times 10 + 0 \times 1 + 2 \times 0.1 = 1 \times 10^2 + 5 \times 10^1 + 0 \times 10^0 + 2 \times 10^{-1}$$

---

# Positional Number System (cont.)

## Representation

$$\pm (\alpha\_{k-1} \cdots \alpha\_2 \alpha\_1 \alpha\_0 . \alpha\_{-1} \alpha\_{-2} \cdots  \alpha\_{-l} )\_r​$$

$$\Downarrow$$

$$\pm (\alpha\_{k-1} \times r^{k-1} + \cdots + \alpha\_2 \times r^{2} + \alpha\_1 \times r^{1} + \alpha\_0 \times r^{0}$$
$$+ \alpha\_{-1} \times r^{-1} + \alpha\_{-2} \times r^{-2} + \cdots + \alpha\_{-l} \times r^{-l})\_r$$

Where，

- $\alpha$ is the set of **symbols**, 
- $r$ is the **base** (or **radix**) .

---

# Positional Number System (cont.)

## Representation

- $r$ the base of a number system to identify the number of digits used in the number system
- the digits always begin with $0$ and continue through one less than $r$. 
- There are $2$ digits ($0$ and $1$) in binary number system, $8$ digits ($0$ through $7$) in octal number system.

---

# Positional Number System (cont.)

## Maximum value

- The maximum value of a decimal integer that can be represented by $k$ digits for base $r$ :
$r^k - 1$
- For example:

    - $k = 1$, the $\max \ value = 9$
    - $k = 2$,  the $\max \ value = 99$
    - $k = 3$, the $\max \ value = 999$

---

# Decimal System

## The base $r = 10$ and we use ten symbols:

| Arabic numerals  | $0$ | $1$ | $2$ | $3$ | $4$ | $5$ | $6$ | $7$ | $8$ | $9$ |
|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|:---|
| Chinese numerals | 零 $\ \ \ \ $ | 一 $\ \ \ \ $ | 二 $\ \ \ \ $ | 三 $\ \ \ \ $ | 四 $\ \ \ \ $ | 五 $\ \ \ \ $ | 六 $\ \ \ \ $ | 七 $\ \ \ \ $ | 八 $\ \ \ \ $ | 九 $\ \ \ \ $ |
| Chinese financial numerals $\ \ \ \ $| 零 | 壹 | 贰 | 叁 | 肆 | 伍 | 陆 | 柒 | 捌 | 玖 |

## Representation : 

$$\pm (\alpha\_{k-1} \cdots \alpha\_2 \alpha\_1 \alpha\_0 \cdot \alpha\_{-1} \alpha\_{-2} \cdots  \alpha\_{-l} )\_{r=10}$$

$$\Downarrow$$

$$\pm (\alpha_{k-1} \times 10^{k-1} +  \cdots + \alpha_2 \times 10^{2} +  \alpha_1 \times 10^{1} +  \alpha_0 \times 10^{0} $$
$$ + \alpha_{-1} \times 10^{-1} + \alpha_{-2} \times 10^{-2} +  \cdots  + \alpha_{-l} \times 10^{-l}) $$

---

# Decimal System (cont.)

## Example

$$(91.52)\_{10} = + 9 \times 10 + 1 \times 1 + 5 \times 0.1 + 2 \times 0.01 $$ 
$$ = 9 \times 10^1 + 1 \times 10^2 + 5 \times 10^{-1} + 2 \times 10^{-2} $$

---

# Binary System

- All data in modern computers is stored as **series of bits**. 
- <mark>A bit is a **binary** digit</mark>. 

## The base $r = 2$ and we use two symbols:

$$ 0, 1 $$

## Representation :

$$\pm (\alpha\_{k-1} \cdots \alpha\_2 \alpha\_1 \alpha\_0 \alpha\_{-1} \alpha\_{-2} \cdots  \alpha\_{-l} )\_{r=2}$$

$$\Downarrow$$

$$\pm (\alpha_{k-1} \times 2^{k-1} +  \cdots + \alpha_2 \times 2^{2} +  \alpha_1 \times 2^{1} + \alpha_0 \times 2^{0}$$
$$ + \alpha_{-1} \times 2^{-1} + \alpha_{-2} \times 2^{-2} + \cdots + \alpha_{-l} \times 2^{-l})$$

---

# Binary System (cont.)

## Example

$$(110.01)\_2 = 1 \times 2^2 + 1 \times 2^1 + 0 \times 2^0  + + 0 \times 2^{-1} + 1 \times 2^{-2}$$

$$\Downarrow$$

| Place values $\ \ \ \ $ | $2^2$ $\ \ \ \ $ | $2^1$ $\ \ \ \ $ | $2^0$ $\ \ \ \ $ | $2^{-1}$ $\ \ \ \ $ | $2^{-2}$ $\ \ \ \ $ |
| :----------- | :----- | :----- | :-------- | :-------- | :-------- |
| Number       | 1      | 1      | 0         | 0         |1|

$$\Downarrow$$

value (in decimal)   :  $R =  1 * 2^2 + 1* 2^1 + 0 * 2^0  + + 0 * 2^{-1} + 1 * 2^{-2} $


<!---
The most basic form of representing computer data, then, is to represent a piece of data as a string of 1s and 0s, one for each bit. What you end up with is a binary or base-2 number; this is binary notation. 

The example of real number $(110.01)\_2$  

value:  $R =  1 * 2^2 + 1* 2^1 + 0 * 2^0  + + 0 * 2^{-1} + 1 * 2^{-2} $

$$\Downarrow$$

--->

---

# Binary System (cont.)

## <mark>Bit is the smallest unit of the binary system. </mark>

- in the real applications, one prefers to use **byte** (**B**), which equals 8 bits, to measure the capacity of a storage device, or a memory chip or a binary number stored in the computer. 
- If the capacity or the number is very large, one has to prefix a letter to the **byte** (**B**) to save space.  

|Unit ( Prefix ) || Bytes (B) in binary | | Roughly  Bytes (B) in decimal | Exact bits(Notes) |
|:---|:---|:---|:---|:---|:---|
|B  |Byte (字节)| $2^0$| 1 | $10^0$| 8|
|KB |Kilo (千)  | $2^{10}$| 1024| $10^3$| 8192|
|MB |Mega (兆)  | $2^{20}$| 1,048,576| $10^6$| 8,388,608|
|GB |Giga (吉)  | $2^{30}$| 1,073,741,824| $10^9$| 8,589,934,592|
|TB |Tera (太)  | $2^{40}$| 1,099,511,627,776| $10^{12}$| 8,796,093,022,208 (**Mass data, 海量数据**)|
|PB |Peta (拍)  | $2^{50}$| 1,125,899,906,842,624| $10^{15}$| 9,007,199,254,740,992|
|EB |Exa (艾)   | $2^{60}$| 1,152,921,504,606,846,976| $10^{18}$| 9,223,372,036,854,775,808|
|ZB |Zetta(泽)  | $2^{70}$| 1,180,591,620,717,411,303,424| $10^{21}$| 9,444,732,965,739,290,427,392 (**Big data, 大数据**)|

<!---
|YB |Yotta【尧】 | $2^{80}$| 1024ZB| $10^{24}$| 8192Z|
|BB |Bronto【博】| $2^{90}$| 1024YB| $10^{27}$| 8192Y|
|NB |Nona【诺】  | $2^{100}$| 1024BB| $10^{30}$| 8192B|
|DB |Dogga【多】 | $2^{110}$| 1024NB| $10^{33}$| 8192N|
|CB |Corydon【稞】|$2^{120}$| 1024DB| $10^{36}$| 8192D|
--->

---

# Hexadecimal System

## Because Binary System can be cumbersome for human being, two more compact notations are often used, **Octal** and **Hexadecimal**. 

## The Hexadecimal System uses the base $r=16$, representing <mark>__four bits__</mark> with each digit.

- ten base-$10$ digits ($0 \sim 9$) 
- the letters $A \sim F$ (representing the numbers $10 \sim 15$). <br>
(<mark>The symbols $A$, $B$, $C$, $D$, $E$, $F$ represent the values of $10$, $11$, $12$, $13$, $14$, $15$ respectively.</mark>)

## Representation :

$$\pm ( \alpha\_{k-1} \alpha\_{k-2} \cdots \alpha\_2 \alpha\_1 \alpha_0 )\_{r = 16}$$

$$\Downarrow$$

$$\pm (\alpha_{k-1} \times 16^{k-1} + \alpha_{k-2} \times 16^{k-2} +  \cdots + \alpha_2 \times 16^{2} +  \alpha_1 \times 16^{1} +  \alpha_0 \times 16^{0})$$

---

# Hexadecimal System (cont.)

## Example

$$ (3BD)\_{16} =  3 \times 16^2 + B \times 16^1 + D \times 16^0 \\ =  3 \times 16^2 + 11 \times 16^1 + 13 \times 16^0 $$

$$\Downarrow$$

| Place values $\ \ \ \ $ | $16^2$ $\ \ \ \ $ | $16^1$ $\ \ \ \ $ | $16^0$ $\ \ \ \ $ |
| :----------- | :----- | :----- | :-------- |
| Number       | 3      | B      | D         |

$$\Downarrow$$

value (in decimal)   : $N =  3 * 16^2 + 11* 16^1 + 13 * 16^0 $

<!---
The example of number 

| Place values | $16^2$ | $16^1$ | $16^0$ |
| :----------- | :----- | :----- | :-------- |
| Number       | 3      | B      | D         |

value:  $N =  3 * 16^2 + 11* 16^1 + 13 * 16^0 $
--->

---

# Octal System

## Octal notation uses the base $r=8$, representing <mark>__three__ bits</mark> with each digit. 

- eight base-$10$ digits ($0 \sim 7$) <br>
- ($0, 1, 2, 3, 4, 5, 6, 7$)

## Representation :

$$\pm ( \alpha\_{k-1} \alpha\_{k-2} \cdots \alpha\_2 \alpha\_1 \alpha\_0 )\_{r=8}$$

$$\Downarrow$$

$$\pm (\alpha_{k-1} \times 8^{k-1} + \alpha_{k-2} \times 8^{k-2} +  \cdots + \alpha_2 * 8^{2} +  \alpha_1 \times 8^{1} +  \alpha_0 \times 8^{0})$$


## Example

$$(2147)\_8 = 2 \times 8^3 + 1 \times 8^2 + 4 \times 8^1 + 7 \times 8^0$$

<!---
The example of real number $(2147)\_8$

| Place values | $16^3$ | $16^2$ | $16^1$ | $16^0$ |
| :----------- | :----- | :----- | :----- | :-------- |
| Number       | 2      | 1      | 4         | 7|

value:  $N =  2 * 8^3 + 1 * 8^2 + 4* 8^1 + 7 * 8^0 $
--->

---

# Summary 

## The four positional number systems

| Number system $\  \  \  \ $| base | Symbols | Examples |
|:--- |:--- |:--- |:--- |
| Decimal | $r=10$ | $0,1,2,3,4,5,6,7,8,9$ | 2223.89 |
| Binary  | $r=2$  | $0,1$ | $(1110.01)\_2$ |
| Octal   | $r=8$  | $0,1,2,3,4,5,6,7$ | $(7116.02)\_8$ |
| Hexadecimal | $r=16$ $\  \  \  \ $| $0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F$ $\  \  \  \ $| $(FC2.2E)\_{16}$ |

---

# Summary (cont.)

## Comparison of numerals in the four systems

| Decimal $\  \ \  \  \ $ |  Hexadecimal $\  \ \  \  \ $ | Octal $\  \ \  \  \ $ |  $\  \ \  \  \ $Binary  |
| :---: | :---: | :---: | :---: |
| 0| 0| 0| 0000| 
| 1| 1| 1| 0001| 
| 2| 2| 2| 0010| 
| 3| 3| 3| 0011| 
| 4| 4| 4| 0100| 
| 5| 5| 5| 0101| 
| 6| 6| 6| 0110| 
| 7| 7| 7| 0111| 
| 8| 8| 10| 1000|
| 9| 9| 11| 1001|
| 10| A| 12| 1010|
| 11| B| 13| 1011|
| 12| C| 14| 1100|
| 13| D| 15| 1101|
| 14| E| 16| 1110|
| 15| F| 17| 1111|

---

# Practice Set

## Choice questions :

1. The base of the decimal number system is \_\_\_\_\_\_\_<br>
a) $8$; b) $2$; c) $16$; d) $10$

2. Which of the following representation is incorrect? \_\_\_\_\_\_\_<br>
a) $(11010010)\_2$; b) $(944)\_8$; c) $(4FB)\_{16}$; d) $3552$

3. Which of the following is equivalent to $13$ in decimal? \_\_\_\_\_\_\_<br>
a) $(1101)\_2$; b) $(17)\_8$; c) $(F)\_{16}$; d) none of the above

---

# Practice Set (cont.)

## Calculations questions :

1. Convert the following binary numbers to decimal: <br>
a) $(11001110)\_2$; <br>
b) $(101101)\_2$; <br>
c) $(10110.101)\_2$; <br>
d) $(100111.111)\_2$<br>

2. Convert the following hexadecimal numbers to decimal: <br>
a) $(AC2)\_{16}$; <br>
b) $(123)\_{16}$; <br>
c) $(ABB)\_{16}$; <br>
d) $(35E.E1)\_{16}$<br>

---

# Practice Set (cont.)

## Questions :

1. What is number system？
2. Explain some basic concepts about a number system.
3. How many bits in a binary system are represented by one digit in the Hexadecimal system?
4. How many bits in a binary system are represented by one digit in the octal system?

## Note: 
- Please bring your own answer sheet; 
- Please indicat **your name** and **student number** on your answer sheet;
- <mark>**Your answer sheet must be submitted at the end of this class time.**</mark>

- International students:  Please submit your electronic answer sheet to **bushehui@qq.com** before 9pm(BJT).

---

# Conversion

---

# Conversion from other bases to decimal

## Procedure :
- Step. 1: Determine the place value of each digit
- Step. 2: Multiply each digit with its corresponding place value 
- Step. 3: Add the results of the products to get the equivalent number in decimal

## The number from $r$ bases system :

$$\pm (\alpha\_{k-1} \cdots \alpha\_2 \alpha\_1 \alpha\_0 \cdot \alpha\_{-1} \alpha\_{-2} \cdots  \alpha\_{-l} )\_r$$
$$\Downarrow$$
![ConvertingToDec](figs/ConvertingToDec.png)

---

# Example 

## Ex $1$ : $(101.01)\_2$

$$(101.01)\_2 = 1 \times 2^2 + 0 \times 2^1 + 1 \times 2^0 + 0 \times 2^{-1} + 1 \times 2^{-2}$$
$$\Downarrow$$
$$ 4 + 0 + 1 + 0 + 0.25 = 5.25 $$

<br>
<br>

## Ex $2$ : $(2B.48)\_{16}$

$$(2B.48)\_{16} = 2 \times 16^1 + B \times 2^0 + 4 \times 16^{-1} + 8 \times 16^{-2}$$
$$\Downarrow$$
$$ 2 \times 16^1 + 11 \times 2^0 + 4 \times 16^{-1} + 8 \times 16^{-2}$$
$$\Downarrow$$
$$ 32 + 11 + 0.25 + 0.03125 = 43.28125 $$

<!---
# Converting from other bases into decimal

The example of converting the binary number $(101.01)\_2$ to decimal: $(101.01)\_2 = 5.25$.

| Binary | $1$ | $0$ | $1$ | $0$ | $1$ |
| :----------- | :----- | :----- | :----- | :-------- | :-------- |
| Place values | $2^2$ | $2^1$ | $2^0$ | $2^{-1}$ | $2^{-2}$ |
| Decimal       | 4      | +  0      |  + 1   | + 0 | + 0.25 = 5.25 |
--->

---

# Conversion from decimal to other bases

## Two processes : 

- **Process I** : Converting the integral part<br>
    - Use the skill of repetitive __division__ to convert the integral part

<br>

-  **Process II** : Converting the fractional part<br>
    - Use the skill of repetitive __multiplication__ to convert the fractional part

<!---
When converting the integral part of the specified number, we use the skill of repetitive division to convert the integral part.
When converting fractional part of the specified number, we use the skill of repetitive multiplication to convert the fractional part.
--->

---

# Converting the integral part


## Frame work of the the repetitive dividion :

<img src="figs/ConvertingInt.png" alt="ConvertingInt" width="750">

---

# Converting the integral part (cont.)

<img src="figs/ConvertingInt2.png" alt="ConvertingInt2" width="750">

<!---
![Roman numerals](figs/ConvertingInt.png)

![Roman numerals](figs/ConvertingInt2.png)

![Roman numerals](figs/Converting_ex_1.png)
--->

---

# Example 

## Convert $(47)\_{10}$ in decimal to binary.

<img src="figs/Converting_ex_1.png" alt="Converting_ex_1" width="500">

- Step 1 : $47 = 23 \times 2 + 1$ 
- Step 2 : $23 = 11 \times 2 + 1$ 
- Step 3 : $11 = 5 \times 2 + 1$ 
- Step 4 : $5 = 2 \times 2 + 1$  
- Step 5 : $2 = 2 \times 1 + 0$ 
- Step 6 : $2 = 2 \times 0 + 1$ 

## The result : $47 = (101111)\_2$

---

# Converting the fractional part

## Frame work of the the repetitive multiplication :

<img src="figs/ConvertingFrac.png" alt="ConvertingFrac" width="400">

<img src="figs/ConvertingFrac2.png" alt="ConvertingFrac2" width="400">

---

# Example 

## Convert $0.375$ in decimal to binary.

<img src="figs/Converting_ex_2.png" alt="Converting_ex_2" width="500">

- Step 1 : $0.375 \times 2 = 0.75 = 0 + 0.75$
- Step 2 : $0.75  \times 2 = 1.50 = 1 + 0.5$
- Step 3 : $0.50  \times 2 = 1.00 = 1 + 0.00$

# The result : $(0.375)\_{10} = (0.011)\_2$

---

# Example (cont.)

## Convert $0.347$ in decimal to octal.

<img src="figs/Converting_ex_3.png" alt="Converting_ex_3" width="500">

- Step 1 : $0.374 \times 8 = 2.992 = 2 + 0.992$
- Step 2 : $0.992 \times 8 = 7.936 = 7 + 0.936$
- Step 3 : $0.936 \times 8 = 7.488 = 7 + 0.488$
- Step 4 : $0.488 \times 8 = 3.904 = 3 + 0.904$

## The result : $(0.347)\_{10} = (0.2773)\_8$

---

# Example (cont.)

## Convert $195.4$ in decimal to hexadecimal.

<img src="figs/Converting_ex_4.png" alt="Converting_ex_4" width="500">

- Step 1 : $195.4 = 195 + 0.4$
- Step 2.1 : $195 = 12 \times 16 + 3$ 
- Step 2.2 : $12 = 0 \times 16 + 12 = C$ 
- Step 3 : $0.4 \times 16 = 6.4 = 6 + 0.4$

## The result ： $(195.4)\_{10} = (C3.6)\_{16}$

---

# Binary-Hexadecimal Conversion

## <mark>Four bits is one hexadecimal digit. </mark>

<img src="figs/ConvertingHexBin.png" alt="ConvertingHexBin" width="450">

## Example : $(10110101001)\_2$

- Arrange the binary number in $4$-bit patterns : $(10110101001)\_2 = (0101 \ \ 1010 \ \ 1001)\_2$
- Convert the $4$-bit pattern binary into one hexadecimal digit
    - $(0101)\_2 = (5)\_{16}$
    - $(1010)\_2 = (A)\_{16}$
    - $(1001)\_2 = (9)\_{16}$ 
- $(10110101001)\_2 = (5A9)\_{16}$

---

# Binary-Octal conversion

## Similar to the Binary-Hexadecimal Conversion : <mark>three bits is one octal digit.</mark>

<img src="figs/ConvertingOctBin.png" alt="ConvertingOctBin" width="450">

## Example : $(111101011)\_2$

- Arrange the binary number in $3$-bit patterns:  $(111101011)\_2 = (111 \  101 \  011)\_2$
- Convert the $3$-bit pattern binary into one Octal digit
    - $(111)\_2 = (7)\_8$
    - $(101)\_2 = (5)\_8$
    - $(011)\_2 = (3)\_8$
- $(111101011)\_2 = (753)\_8$

---

# Octal-Hexadecimal Conversion

## Procedure :

- __First step__  : The specified number is first translated into equivalent the __binary number__
- __Second step__ : The __binary number__ is converted to the representation in the target number system

## Example:  conversion between $(6572)\_8$ and $(D7A)\_{16}$

<img src="figs/Converting_ex_5.png" alt="Converting_ex_5" width="550">

---

# Non-Positional  Number System

## Basic about non-positional number system

- Unlike the numbers in positional number system, **the position of symbols in a number normally has no relation to its value**.
- <mark> Modern computers do not use non-positional number systems, </mark>mark> and the computer data are stored using binary.

Representation ：

$$\pm (\alpha_{k-1} \cdots \alpha_2 \alpha_1 \alpha_0 \cdot \alpha_{-1} \alpha_{-2} \cdots  \alpha_{-l} ) r$$

Value ：
$$
n = \pm (\alpha_{k-1} + \cdots + \alpha_2 + \alpha_1 + \alpha_0) + (\alpha_{-1} + \alpha_{-2} + \cdots + \alpha_{-l} )
$$

---

# Roman numerals 

- This number system is based on a set of seven different symbols $S = {I, V, X, L, C, D, M}$. 
- The symbols of Roman numerals and their values :

|Symbol  $\ \ \ \ $  |$I$   |$V$   |$X$   |$L$   |$C$   |$D$   |$M$|
|:---  |:---|:---|:---|:---|:---|:---|:---|
|Value |$1$  $\ \ \ \ $ |$5$  $\ \ \ \ $ |$10$ $\ \ \ \ $ |$50$ $\ \ \ \ $ |$100$ $\ \ \ \ $ |$500$ $\ \ \ \ $|$1000$ $\ \ \ \ $|

In order to calculate the value of a roman numeral, we must follow its specific rules:

1. When same symbols are written together, the values are added, such as $III = 1 + 1 + 1 = 3$.
2. When a symbol with a larger value is placed on the left of a symbol with smaller value, the values are added, such as $VI = 5 + 1 = 6$; $VII = 5+1+1=7$; $VIII=5+1+1+1=8$
3. When a symbol with a larger value is placed on the right of a symbol with a smaller value, the smaller value is subtracted from the larger one, such as $IX = 10 - 1$.
4. When a bar is placed over a symbol, it means multiplying the value with $1000$, such as $I = 1000$.

---

# Roman numerals (cont.)

## Some Roman numerals and their values.

<img src="figs/RomanNumerals.png" alt="RomanNumerals" width="650">

---

# Summary

## Numbers consist of several symbols in the number system.
- Number systems can be approximately classified into two systems: positional number system and non-positional number system.
    - In a positional number system, the position of a symbol in the number presentation has its own specific value, which is called a place value.
    - In a non-positional number system, every symbol have specific values, but the position of a symbol in the number presentation has no relationship with its value.

---

# Summary (cont.)

- In a decimal system, the base equals 10 and there are 10 symbols. The symbols are regarded as decimal digits.
- In a binary system, the base equals 2 and there are just 2 symbols. The symbols are regarded as binary digits.
- In a hexadecimal system, the base equals 16 and there are 16 symbols. The symbols are regarded as hexadecimal digits.
- In an octal system, the base equals 8 and there are 8 symbols. The symbols are regarded as octal digits.

---

# Summary (cont.)

- In the process of converting a number in any number system to a decimal number, we multiply each digit with its corresponding place value, and add them together to obtain the result.
    - When we convert a real, we need two steps: one is converting the integral part of the real; another is converting the fraction part of the real. The former uses repetitive division, the latter uses repetitive multiplication.
    - Because four digits in a binary system can be represented by one digit in a hexadecimal system, we can use this relationship to solve the problems of conversion between a binary system and a hexadecimal system.
    - Similar to the conversion between a binary system and a hexadecimal system, as three digits in a binary system can be represented by one digit in an octal system, we can make full use of this relationship to solve the problems of conversion between a binary system and an octal system.
    - In the process of conversion between an octal system and a hexadecimal system, we can make full use of the binary-octal relationship and binary–hexadecimal relationship to realize our goal.

---

# Practice Set

## Calculations questions :

2. Convert the following hexadecimal numbers to decimal: \_\_\_\_\_\_\_<br>
a) $(AC2)\_{16}$; b) $(123)\_{16}$; c) $(ABB)\_{16}$; d) $(35E.E1)\_{16}$

3. Convert the following octal numbers to decimal :  \_\_\_\_\_\_\_<br>
a) $(437)\_8$; b) $(2271)\_8$; c) $(223.7)\_8$; d) $(471.21)\_8$

4. Convert the following decimal numbers to binary : \_\_\_\_\_\_\_<br>
a) $1314$; b) $21$; c) $314.02$; d) $14.56$

5. Convert the following decimal numbers to octal: \_\_\_\_\_\_\_<br>
a) $1756$; b) $346$; c) $121.4$; d) $48.8$

---

# Practice Set (cont.)

## Calculations questions :

6. Convert the following decimal numbers to hexadecimal: \_\_\_\_\_\_\_<br>
a) $717$; b) $121$; c) $212.13$; d) $316.5$

7. Convert the following octal numbers to hexadecimal: \_\_\_\_\_\_\_<br>
a) $(514)\_8$; b) $(411)\_8$; c) $(13.7)\_8$; d) $(1256)\_8$


8. Convert the following decimal numbers to binary: \_\_\_\_\_\_\_<br>
a) $4 \ \frac{5}{8}$; b) $2 \ \frac{3}{32}$; c) $14 \ \frac{13}{64}$; d) $22 \ \frac{5}{128}$

9. Find the maximum value of an integer in each of the following cases: \_\_\_\_\_\_\_<br>
a) $b=10$, $k=10$; b) $b=2$, $k=12$; c) $b=8$, $k=8$; d) $b=16$, $k=7$

10. Write the decimal equivalents of the following Roman numbers: \_\_\_\_\_\_\_<br>
a) $XXVII$; b) $XV$; c) $MCLVII$; d) $VLIII$

---

# Practice Set (cont.)

## Questions :

1. Explain the main idea of conversion between an octal system and a hexadecimal system.

## Note: 
- Please bring your own answer sheet; 
- Please indicat **your name** and **student number** on your answer sheet;
- <mark>**Your answer sheet must be submitted at the end of this class time.**</mark>

- International students:  Please submit your electronic answer sheet to **bushehui@qq.com** before 9pm(BJT).

---

# QQ Group

<img src="figs/QQ-Group.jpg" alt="QQ-Group" width="300">

## Chinese students :  Please join this QQ group

## International students :  Not need to join this QQ group

<!---
landslide file.md -i -m -o > file.html
landslide file.md -i -x tables -m -o > file.html
--->
