# An Introduction to Computer Science <br> (Foundations of Computer Science) <br> 计算机科学导论

---

# Unit 3 <br> Data Storage and Compression <br> 第三章 <br> 数据存储与压缩

---

# OBJECTIVES

## You are supposed to be able to :
- **Understand the uniform representation inside the computer  for different data types.**
- **Understand the different representations of an integer inside a computer: <mark>unsigned, sign-and-magnitude, one’s - complement, and two’s complement</mark>.**
- <mark>**Understand the Excess system that is used to store the exponential part of a floating-point number.**</mark>
- <mark>**Understand how floating numbers are stored inside a computerusing the exponent and the mantissa.**</mark>
- Understand how **different types of data** are represented and compressed inside the computer.
- Understand the new network storage technology – **cloud storage**.   
- Understand the main storage technologies for **big data**.   

---

# Bit Pattern (位模式/位组)


## The computers are 

- used to scientific calculations and <mark>display human-readable text</mark>.
- actually <mark>multimedia devices</mark>, dealing with many different types of data, including **numbers**, **text**, **audio**, **images**, and **video**. 

$$\Downarrow$$

- For efficiency, all aforementioned data types have a uniform representation inside the computer, which is based on a **binary system**, called a <mark>bit pattern (位模式/位组)</mark> or <mark>binary representation (二进制表示)</mark>.

<br>

$$10111111$$

- In fact, there have been computers based on decimal number system or other number systems. **But these computers are too complicated, expensive, and less stable for every day use. **

---

# Bit Pattern (cont.)

## <mark>If a single logic unit represents less possible values, the computer will be more stable.</mark> 
- For an electronic signal, the binary system provides only two possible states: low or high, corresponding to $0$ or $1$ respectively. 
- An electronic switch can be easily represented by two stable states of electronic signal. 
- These sates can be defined as on and off represented by $1$ and $0$ respectively. 

<img src="figs/switch.gif" alt="switch" width="70">

## To represent more than two things (**on** and **off**), one bit is not enough, so we need a sequence of bits. 
- In general, $m$ bits are capable of representing $2^m$ things because $m$ bits can make $2^m$ combinations of $0$ and $1$. 

---

# Bit Pattern (cont.)

## Computer memory (内存) has no idea what type of data a stored bit pattern represents. 

- The memory stores various pieces of data with different patterns according to their data types (内存使用不同的模式，根据数据类型，存储多份数据).
- For example :

<img src="figs/TableBitEx.png" alt="TableBitEx" width="500">

---

# Integer in Computer

---

# Integer 

## It’s natural to use a bit pattern to represent integers. 

- Integers represent numbers which have no fractional part. 
- Each bit pattern can be treated as a binary number, and each binary number can be converted to the corresponding decimal integer. 

<br>

## A fixed-point representation (定点表示法) is the method used for storing integers in binary format. 

- The decimal point is assumed at the right of the least significant (rightmost) bit (最低有效位； 最右位) without any gap. 

<img src="figs/IntBit.png" alt="IntBit" width="500">

---

# Unsigned/Signed Integer 

## To make more efficient use of computer memory, unsigned integer (无符号整数) and signed integer (有符号整数) have been developed as two categories of integer representation. 

## Three distinct ways have been developed to represent signed integers： 
- Sign-and-Magnitude (原码) 
- One’s Complement (二进制反码/一的补码)
- Two’s Complement (二进制补码)

<img src="figs/IntType.png" alt="IntType" width="500">

---

# Unsigned representation

## The biggest difference between a signed and unsigned integer number is that **the far left bit** is used to denote whether or not the number has a negative sign. 

- Unsigned representation do not require the **the far left bit** (**the sign bit** or **the arithmetic sign**)
- Unsigned representation is used to represent positive integers and zero (natural number). 
- The value of an unsigned integer is interpreted as "**the magnitude of its underlying binary pattern**".

---

# Unsigned representation (cont.)

## An $n$-bit pattern can represent $2^n$ distinct integers. 
- An $n$-bit unsigned integer can represent integers from $0$ to $(2^n)-1$, as tabulated below:

| n    | Minimum $\ \ \ $ |	Maximum |
| :--- | :---:   | :---     |
| $8$  |	$0$	 | $(2^8) - 1 = 255 $ |
| $16$ |	$0$	 | $(2^{16}) - 1 = 65,535$ |
| $32$ |	$0$	 | $(2^{32}) - 1 = 4,294,967,295$ |
| $64$ $\ \ \ $|	$0$	 | $(2^{64}) - 1 = 18,446,744,073,709,551,615$|

---

# Signed representation

## The biggest difference between a signed and unsigned integer number is that **the far left bit** (the **sign bit** or the **arithmetic sign**) is used to denote whether or not the number has a negative sign. 

- If the sign bit is equal to $0$, the signed representation is **positive**,
and its convention is the same as an unsigned representation
- If the sign bit is equal to $1$, thw signed representation is **negative**
- The remaining bits represent the actual number. 
The remaining $n-1 $bits represents the magnitude (absolute value) of the integer. 
The absolute value of the integer is interpreted as "the magnitude of the $(n-1)$-bit binary pattern"

---

# Signed representation  (cont.)

## Example :
- ** 1**:  Suppose that $n=8$ and the binary representation is $(0 100 0001)\_2$.<br>
    - Sign bit is $0$ $\Rightarrow$ **positive**,<br>
    - Absolute value is $(100 0001)\_2 = (65)\_{10}$.<br>
    - Hence, the integer is $+65$.

- ** 2**:  Suppose that $n=8$ and the binary representation is $(1 000 0001)\_2$.<br>
    - Sign bit is $1$ $\Rightarrow$ **negative**,<br>
    - Absolute value is $(000 0001)\_2 = (1)\_{10}$.<br>
    - Hence, the integer is $-1$.

---

# Sign-and-magnitude (原码)

## Sign-and-magnitude representation is simple. 
- We can transform its magnitude part to decimal value directly. 
- Example of sign-and-magnitude representation with $5$-bit allocation :
    - Since only $4$ bits can be used to represent the magnitude part, 
    - this range is divided into two halves: $00000$ to $01111$ (represents positive integers) and $10000$ to $11111$ (represents negative integers). 

<img src="figs/Sign-And-Magnitude.png" alt="Sign-And-Magnitude" width="750">

---

# Sign-and-magnitude (cont.)

<img src="figs/DataRep_SignMagnitude.png" alt="DataRep_SignMagnitude" width="400">

- Two zeros: $+0$ and $-0$. 
    - We often ignore the negative zero entirely, but within the computer, it may cause unnecessary complexity. 
    - It’s easy to conclude that an $m$-bit location can represent numbers from $-(2^{m-1}-1)$ to $+(2^{m-1}-1)$

---

# One’s complement  

## One’s complement (二进制反码/一的补码) representation of a negative binary integer is the complement of its positive counterpart. 

- For a positive integer, same with sign-and-magnitude representation
- For a negative integer, the **sign bit** is equal to $1$,  its complement is obtained by <mark> changing all bits of $0$s to $1$s and all bits of $1$s to $0$s</mark>. 
- The range of signed integers using one’s complement in a computer is the same as the range of sign-and-magnitude integers. 

<img src="figs/Sign-And-Magnitude2.png" alt="Sign-And-Magnitude2" width="750">

---

# One’s complement (cont.)

| One’s complement | Sign-and-magnitude |
|:---:|:---:|
|<img src="figs/DataRep_OneComplement.png" alt="DataRep_OneComplement" width="400">|<img src="figs/DataRep_SignMagnitude.png" alt="DataRep_SignMagnitude" width="400">|

- There are also two representations of $0$ in this format, denoted by $-0$ (negative zero) and $+0$ (positive zero). 

---

# Example

## Store $–268$ in a $16$-bit memory location using one’s complement representation.

- **Solution** :
<img src="figs/Sign-And-Magnitude_EX1.png" alt="Sign-And-Magnitude_EX1" width="400">

- The **result** : 
$$1111110111110011$$

**Note**: the result is totally different from that for the sign-and-magnitude representation  $100000100001100$!

---

# Two’s complement (二进制补码)

## In fact, two’s complement is the most common method used by computer to represent and store a signed integer with $m$-bit. 

- An unsigned integer of ($0$ to $2m−1$) using two’s complement representation also has two available sub-ranges. 
- Unlike the previous two methods for signed integers, two’s complement has only one representation of zero, and $1000$ is a special case whose leftmost bit $1$ not only represent a negative sign, but also contribute to the decimal value. 
- So the range of numbers that $m$-bit location can store using two’s complement is $-2^{m-1}$ to $+ (2^{m-1} - 1$). 

<img src="figs/Sign-And-Magnitude3.png" alt="Sign-And-Magnitude3" width="750">

- The two’s complement of an integer can also be completed by adding $1$ to the result after taking the complement. 


---

# Two’s complement (cont.)

- If the integer is positive, the conversion from decimal to binary is enough, just like the sign-and-magnitude representation
    - Note that the left padding 0s are still needed if bits are not enough. 

- If the integer is negative, the operation includes two steps. 
    - leave the **rightmost** $0$s up to the **first** $1$ (including the 1) unchanged and then complement the rest. 

---

# Two’s complement (cont.)

<img src="figs/DataRep_TwoComplement.png" alt="DataRep_TwoComplement" width="400">

---

# Example

## Store $–5$ in a $4$-bit memory location using two’s complement representation.

- **Solution**
    - First, ignore the sign of number $5$, change it to binary $101$. 
    - Add one $0$ to make a total of $N (4)$ bits, $0101$. 
    - The sign is negative, so leave the rightmost $0s$ up to the first $1$ (including the $1$) unchanged and complement the rest (or complement $0101 \Rightarrow 1010$, then add $1$ )

<img src="figs/Sign-And-Magnitude_EX2.png" alt="Sign-And-Magnitude_EX2" width="650">

<!---
- The **result** 
$$1011$$

- The following table shows the differences among all these integer representations. 
--->

---

# Two’s complement (cont.)

## This diagram explains how the two's complement works. 

<img src="figs/DataRep_SignedIntegers.png" alt="DataRep_SignedIntegers" width="650">

By re-arranging the number line, values from $-128$ to $+127$ are represented contiguously by ignoring the carry bit.

---

# Summary of Integer Representations 

- In this table, we assume that m is $4$, so the memory location can store only $4$ bits. 

<img src="figs/TableIntegerRepresentations.png" alt="TableIntegerRepresentations" width="550">

**Note** : that the interpretation is different for negative integer, while it is the same for positive integer. 

---

# Excess representation

## Excess representation is also known as biased representation.
- It adds a designated **biased value** (or **magic number**) to the original value to store all exponents as an unsigned integer. 
    - If the exponent occupies $m$ bits in computer memory, the designated biased value is $2^{m−1}-1$ (referred to as $L$). 

## The shifting in excess system with $4$-bit allocation is shown in the following figure. 
- This new system is generally called Excess-$L$, like Excess-$7$.

<img src="figs/ExcessRepresentation.png" alt="ExcessRepresentation" width="500">

---

# Practice Set (I)

1. Change the following $8$-bit unsigned numbers to decimal.  <br>
a) $10010100$; b) $01101011$; c) $11111001$; d) $10101111$

2. The following numbers are sign-and-magnitude binary numbers in an $8$-bit allocation. Convert them to decimal.  <br>
a) $10001000$; b) $00000011$; c) $10001011$; d) $00110001$

3. Use sign-and-magnitude with $8$-bit allocation to represent the following decimal integers.  <br>
a) $53$; b) $-107$; c) $-5$; d) $154$

4. Change the following decimal numbers to $8$-bit two'scomplement integers.  <br>
a) $82$; b) $-119$; c) $53$; d) $126$

---

# Floating-Point in Computer

---

# Floating-Point

## A number which consists of <mark>an integral part</mark> and <mark>a fractional part</mark> is called a real (实数). 
- We can use **fixed-point representation** to represent a real number, however, <mark>the result is hard to be accurate enough because **the digits in integral part and fractional part are both fixed**</mark>
- Since computer memory is limited, you cannot store numbers with infinite precision 
$$\Downarrow$$
- The solution is to use **floating-point representation** (浮点表示法)

---

# Floating-Point (cont.)

## Floating-point representation adopts **scientific notation**, with only one non-zero digit to the left of the decimal point “**.**” 

- To satisfy the accuracy for numbers at very different magnitudes
- To satisfy the calculation involved numbers with different magnitudes.

<!---
- In the binary system, this digit can only be 1.

To satisfy the engineer and the chip designer, a number format has to provide accuracy for numbers at very different magnitudes. However, only relative accuracy is needed. To satisfy the physicist, it must be possible to do calculations that involve numbers with different magnitudes.

Basically, having a fixed number of integer and fractional digits is not useful - and the solution is a format with a floating point.
--->

<https://en.wikipedia.org/wiki/Floating-point_arithmetic>

---

# Floating-Point (cont.)

- A floating-point number (or real number) can represent a very large ($1.23 \times 10^{88}$) or a very small ($1.23 \times 10^{-88}$) value
- It could also represent very large negative number ($-1.23 \times 10^{88}$) or very small negative number ($-1.23 \times 10^{88}$), as well as **zero**

<img src="figs/Representation_FloatingPointNumbers.png" alt="Representation_FloatingPointNumbers" width="600">

- A floating-point number is typically expressed in the **scientific notation**, with a **fraction** ($F$), and an **exponent** ($E$) of a certain radix ($r$), in the form of $F \times r^E$.
    - Decimal numbers use radix of $10$ ($F \times 10^E$); 
    - Binary numbers use radix of $2$ ($F \times 2^E$).

<!---
Representation of floating point number is not unique. For example, the number 55.66 can be represented as 5.566×10^1, 0.5566×10^2, 0.05566×10^3, and so on. The fractional part can be normalized. 
In the normalized form, there is only a single non-zero digit before the radix point. 
For example, decimal number 123.4567 can be normalized as 1.234567×10^2; binary number 1010.1011B can be normalized as 1.0101011B×2^3.

It is important to note that floating-point numbers suffer from loss of precision when represented with a fixed number of bits (e.g., 32-bit or 64-bit). This is because there are infinite number of real numbers (even within a small range of says 0.0 to 0.1). 
On the other hand, a n-bit binary pattern can represent a finite 2^n distinct numbers. Hence, not all the real numbers can be represented. The nearest approximation will be used instead, resulted in loss of accuracy.

It is also important to note that floating number arithmetic is very much less efficient than integer arithmetic. It could be speed up with a so-called dedicated floating-point co-processor. Hence, use integers if your application does not require floating-point numbers.

- In computers, floating-point numbers are represented in scientific notation of fraction ($F$) and exponent ($E$) with a radix of $2$, in the form of $F \times 2^E$. 
- Both $E$ and $F$ can be positive as well as negative. 
- Modern computers adopt IEEE 754 standard for representing floating-point numbers. 
There are two representation schemes: 32-bit single-precision and 64-bit double-precision.

--->

---

# Floating-Point (cont.)

## Such a format satisfies all the requirements:
- It can represent numbers at wildly different **magnitudes** (limited by the length of the exponent)
- It provides the same **relative accuracy** at all magnitudes (limited by the length of the fraction)
- It allows calculations across magnitudes: multiplying a very large and a very small number preserves the accuracy of both in the result.

## The exponent is either written explicitly including the base, or an $e$ is used to separate it from the fraction.

| Fraction $\ \ \ $ | Exponent $\ \ \ $ | Scientific notation $\ \ \ $ | Fixed-point value |
| :--- | :--- | :--- | :--- |
|$1.5$    | $4$   | $1.5 \times 10^4$    |  $15000$  |
|$-2.001$ | $2$   | $-2.001 \times 10^2$ |  $-200.1$ |
|$5$      | $-3$  | $5 \times 10^{-3}$    |  $0.005$  |
|$6.667$  | $-11$ | $6.667 e -11$      |  $0.00000000006667$ |

---

# Floating-Point (cont.)

As shown in the figure, the process of converting a real ($(101100010.01)\_2$ in the following example to **scientific notation** is called **normalization**. 

<img src="figs/Floating-PointExample.png" alt="Floating-PointExample" width="500">

## After **normalization**, only **sign**, **exponent** ( 指数) and **mantissa** (小数部分, **fraction**) need to be stored. 
- Note that the exponent base $2$, leftmost bit $1$, and decimal point in the mantissa are implicit
- <mark> Converting the fraction part of a real number to binary is similar to changing a natural number from base $10$ to base $2$ </mark>, but instead of dividing, it multiply the fraction part by the base. 


<!---
- A **significand** that contains the number’s digits. Negative significands represent negative numbers.
- An **exponent** that says where the decimal (or binary) point is placed relative to the beginning of the significand. Negative exponents represent numbers that are very small (i.e. close to zero).

- The whole number part of the result is the first binary digit to the right of the point. 


## Next, the fractional part of the previous result is multiplied by base $2$. 
- The steps are repeated until the fractional part is **zero** or **until an infinite repeating pattern** is recognized, and then, we have to stop after the required precision is reached.
--->

---

# Example I

## Converting the fraction part

- <mark> Converting the fraction part of a real number to binary is similar to changing a natural number from base $10$ to base $2$ </mark>, but instead of dividing, it multiply the fraction part by the base. 

## Convert $0.25$ from decimal to binary

- **Solution**

    - First, multiply the fraction by $2$; the result is $0.50$. The integer part of the result $0$ is extracted and becomes the leftmost binary digit. 
    - Then, multiply by $2$ the fraction part $0.50$ of the result to get $1.00$. The integer part of the result $1$ is extracted and becomes the next binary digit. 

<img src="figs/ConvertFracPart.png" alt="ConvertFracPart" width="450">

---

# Example II

## Convert the fraction $0.815$ to binary

- **Solution**
    - Write the fraction at the left corner. 
    - Multiply the number continuously by $2$ and extract the integer part as the binary digit. 
    - Stop when the precision is reached.

<img src="figs/Floating-PointExample2.png" alt="Floating-PointExample2" width="450">


Please notice that we have to stop as <mark> it seems that an irregular infinite repetition is occurring </mark>

---

# Example III

## Convert $30.75$ from decimal to binary. 

- First, convert $30$.<br>
    $30$ $\Rightarrow$ $(11110)\_2$ $\ \ \ \ \ \ $ (**placed from right to left!**). 

<img src="figs/Floating-PointExample3.png" alt="Floating-PointExample3" width="500">

- Then, convert the fractional part $0.75$ to binary <br>
    $0.75$ $\Rightarrow$ $(0.11)\_2$

- Therefore, $30.75$ in decimal is $(11110.11)\_2$ in binary.<br>

---

# Practice Set II

1. If the leftmost bit in \_\_\_\_\_\_\_ number representation is $0$, then the decimal number is positive. <br>
a) two's complement; <br> b) floating point; <br> c) excess system; <br> d) both a) and b)

2. If the leftmost bit in \_\_\_\_\_\_\_ number representation is $0$, then the decimal number is positive. <br>
a) two's complement; <br> b) floating point; <br> c) excess system; <br> d) both a) and b)

3. For a fraction part, its exponential value can be stored by which method of number representation? \_\_\_\_\_\_\_ <br>
a) Unsigned integer<br>
b) Two's complement<br>
c) Excess system<br>
d) None of the above

---

# IEEE 754

- In computers, floating-point numbers are represented in scientific notation of fraction ($F$) and exponent ($E$) with a radix of $2$, in the form of $F \times 2^E$. 
    - Both $E$ and $F$ can be positive as well as negative. 
    - Modern computers adopt **IEEE** (**Institute of Electrical and Electronics Engineers**) **FPS** (**Floating-Point Standard**) standard -- **IEEE 754** -- for representing floating-point numbers. 


- **IEEE 754** has defined two standards for storing floating-point numbers in memory: **single precision** ($32$ bits), and **double precision** ($64$ bits). 

| Floating-point numbers’ standards | Sign  $\ \ \ $ | Exponent  $\ \ \ $ | Mantissa  $\ \ \ $ | Smallest number  $\ \ \ $ | Largest number  $\ \ \ $ |
| --------------------------------- | ---- | -------- | -------- | -------- | -------- |
| single precision  ($32$ bits) | $1$ bit $\ \ \ $ | $8$ bits | $23$ bits  | $\approx 1.2 \times 10^{-38}$  | $\approx 3.4 \times 10^{38}$  |
| double precision  ($64$ bits) | $1$ bit $\ \ \ $ | $11$ bits | $52$ bits | $\approx 2.2 \times 10^{-308}$ | $\approx 1.8 \times 10^{308}$ |

---

# IEEE-754 ($32$-bit) 

## Single-Precision Floating-Point Numbers
## In $32$-bit single-precision floating-point representation:

<img src="figs/DataRep_Float32.png" alt="DataRep_Float32" width="500">

- The most significant bit is the sign bit ($S$), with $0$ for positive numbers and $1$ for negative numbers.
- The following $8$ bits represent exponent ($E$).
- The remaining $23$ bits represents fraction ($F$).

<!---
# IEEE 754

- The IEEE standard defines $1$ bit for sign, either $0$ or $1$.
- It defines floating point numbers in their **normalized form**.
- To normalize the mantissa, IEEE standard normalize the fixed-part of a real and use unsigned integer representation to store it. 
- The number of digits used to shift the decimal point to left or right is indicated by the exponent, and this new representation is called **excess representation** (**移码**). 



## The normalized form, 
- the actual fraction is normalized with an implicit leading $1$ in the form of $1.F$. <br>
the actual fraction is $1.011 0000 0000 0000 0000 0000 = 1 + 1×2^{-2} + 1×2^{-3} = (1.375)\_D$.

- The sign bit represents the sign of the number, with $S=0$ for positive and $S=1$ for negative number. <br>
In this example with $S=1$, this is a negative number, i.e., $(-1.375)\_D$.

- the actual exponent is $E-127$ (so-called $excess-127$ or $bias-127$). <br>
This is because we need to represent both positive and negative exponent. With an $8$-bit E, ranging from $0$ to $255$, the $excess-127$ scheme could provide actual exponent of $-127$ to $128$. 
In this example, $E-127=129-127=2D$.

## Hence, the number represented is $-1.375×2^2=-5.5\_D$.


<https://www3.ntu.edu.sg/home/ehchua/programming/java/datarepresentation.html>

<https://www.h-schmidt.net/FloatConverter/IEEE754.html>
--->

---

# IEEE-754 ($32$-bit) example I

## Suppose the $32$-bit pattern is $1 \ 1000 \ 0001\  011 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000$
- $S = 1$
- $E = 1000 0001$
- $F = 011 0000 0000 0000 0000 0000$

## The normalized form :

- the actual fraction is normalized with an implicit leading $1$ in the form of $1.F$. <br>
$\Rightarrow$ the actual fraction is $1.011 0000 0000 0000 0000 0000 = 1 + 1×2^{-2} + 1×2^{-3} = (1.375)\_D$.
- The sign bit represents the sign of the number, with $S=0$ for positive and $S=1$ for negative number. <br>
$\Rightarrow$ this is a negative number, i.e., $(-1.375)\_D$.
- the actual exponent is $E-127$ (so-called excess $-127$ or bias $-127$). <br>
$\Rightarrow$ $E-127=129-127=2\_D$.

---

# IEEE-754 ($32$-bit) example II

## Suppose that IEEE-754 $32$-bit floating-point representation pattern is $0 \ 10000000 \ 110 \ 0000 \ 0000 \ 0000 \ 0000 \ 0000$.

## Solution :

- Sign bit $S = 0$ $\Rightarrow$ positive number
- $E = 1000 0000\_B = 128\_D$ (in normalized form)
- Fraction is $1.11\_B$ (with an implicit leading 1) $\Rightarrow$ $1 + 1×2^{-1} + 1×2^{-2} = 1.75\_D$

## The number is $+1.75 \times 2^{(128-127)} = +3.5\_D$

---

# IEEE 754 example III

## Use IEEE 754 single precision format to represent $-281.875$. 
- For single precision, the number is divided into sign bit, exponent, and fraction (also called **significand** (有效数) or **mantissa** (尾数)). 
- The exponent is encoded as an $8$-bit pattern, so the bias is $127$ (or Excess $-127$). 

## We proceed as follows :

- (1) The sign is negative, so value of sign bit is $1$, that is $S = 1$.
- (2) Transform $281.875$ to decimal: $(100011001.111)\_B$.
- (3) Normalization: $(100011001.111)\_B = (1.00011001111)\_B \times 2^8$.
- (4) $E$ is the exponent field and M is the mantissa. 

$E = 8 + 127 = 135 = (10000111)\_B$ and $M = (00011001111)\_B$. 
We need to add $12$ zeros to the right of $M$ to make it $23$ bits.

---

# IEEE 754 example (III) (cont.)


The representation is shown:

<img src="figs/FinalRepresentation.png" alt="FinalRepresentation" width="500">

- Careful reader may notice that numbers with too small or too large absolute values cannot be stored with this representation. 
- To handle this special case, it is agreed that the value equals $0$ when the sign, exponent and mantissa are all $0$ bits. 
- Excess $-127$ gives an exponent range of $2^{-126}$ to $2^{+127}$, and exponent $0$  $(2^{-127})$ and $255$  $(2^{+128})$ are reserved for special cases. 

---

# IEEE-754 ($64$-bit) 

## Double-Precision Floating-Point Numbers
## The representation scheme for $64$-bit double-precision is similar to the $32$-bit single-precision :

<img src="figs/DataRep_Double64.png" alt="DataRep_Double64" width="500">

- The most significant bit is the sign bit ($S$), with $0$ for positive numbers and $1$ for negative numbers.
- The following 11 bits represent exponent ($E$).
- The remaining 52 bits represents fraction ($F$).

---

# IEEE-754 ($64$-bit) (cont.)

## The value ($N$) is calculated as follows:

- Normalized form: For $1 \le E \le 2046$, $N = (-1)^S × 1.F × 2^{(E-1023)}$.
- Denormalized form: For $E = 0$, $N = (-1)^S × 0.F × 2^{(-1022)}$. <!---These are in the denormalized form.--->
- For $E = 2047$, $N$ represents special values, such as $\pm INF$ (**infinity**), $NaN$ (**not a number**).

<img src="figs/DataRep_Double64.png" alt="DataRep_Double64" width="600">

---

# IEEE-754

## There are three parts in the floating-point representation:

- The sign bit ($S$) is self-explanatory ($0$ for positive numbers and $1$ for negative numbers)
- For the exponent ($E$), a so-called bias (or excess) is applied so as to represent both positive and negative exponent.<br> The bias is set at half of the range
    - For **single precision** with an $8$-bit exponent, the bias is $127$ (or excess$-127$)
    - <mark> For **double precision** with a $11$-bit exponent, the bias is $1023$ (or excess$-1023$)</mark>
- The fraction ($F$) (also called the mantissa or significand) is composed of an implicit leading bit (before the radix point) and the fractional bits (after the radix point) <br>
    - The leading bit for normalized numbers is $1$ 
    - While the leading bit for denormalized numbers is $0$

---

# Summary

- Numbers, text, audio, image and video are five types of data used in a computer. Computer transforms the data into a uniform representation called a bit pattern. 

- Integers represent numbers which have no fractional part. 
- An unsigned integer can never be negative. 
- **Fixed-point** representation is the method used for storing integers. 

- **Sign-and-magnitude** format uses the leftmost bit (Most Significant Bit, also called **sign bit**) to represent the sign, and the rest of the bits define the magnitude. 
- <mark>Two’s complement is the most popular, the most important, and the most widely used way to represent signed integers today.</mark> 
- <mark> A number which combines an integral part with a fractional part is called a real. To store real numbers in computer, the solution is to use floating-point representation, in which a number contains three sections: sign, exponent, and mantissa</makr>. 

---


# Practice Set

1. Change the following $8$-bit two's complement numbers to decimal. \_\_\_\_\_\_\_ <br>
a) $10001000$; b) $00000011$; c) $10001011$; d) $00110001$

2. \_\_\_\_\_\_\_ defines the precision of the fractional part of a number stored in a computer.<br>
a) Exponent; b) Mantissa; c) Sign; d) None of the above

3. Use $32$-bit IEEE format to represent the following numbers. \_\_\_\_\_\_\_ <br>
a) $7.1875$; b) $-12.640625$; c) $11.40625$; d) $-0.375$

4. How a negative integer is represented using two's complement format?
5. How is a real number stored in floating point representation?
6. Compute the largest and smallest negative numbers can be represented in the $32$-bit normalized form and denormalized form.

---

# Practice Set (cont.)

7. Represent the number $(24.076)\_{10}$ in floating point binary representation. <br>Assume the number is $32$bits long using $1$ bit for the sign, $8$ bits for the exponent, and $23$ bits for the mantissa.

8. Compute the largest and smallest positive numbers that can be represented in the $32$-bit normalized form and denormalized form.


## Note: 
- Please bring your own answer sheet; 
- Please indicat **your name** and **student number** on your answer sheet;
- <mark>**Your answer sheet must be submitted at the end of this class time.**</mark>

- International students:  Please submit your electronic answer sheet to **bushehui@qq.com** before 9pm(BJT).

---

# References and Recommended Reading

- Brookshear J G: Computer Science: An Overview, Pearson, 2015
- Dale N and Lewis J: Computer Science Illuminated, Burlington, MA: Jones & Bartlett Learning, 2016.
- Forouzan B A and Mosharraf F: Foundations of Computer Science, Cengage Learning, 2008
- Hadley J: When Online File Storage Gets Legal: Regulatory Compliance, 2014
- Kurdi H, Li M and Al-Raweshidy H S: Taxonomy of Grid Systems. Grid and Cloud Computing: Concepts, Methodologies, Tools and Applications, IGI Global. pages 77-79, 2012
- Miano J: Compressed Image File Formats: JPEG, PNG, GIF, XMB, BMP. Addison-Wesley Professional, 1999
- Murray J D, VanRyper W. Encyclopedia of graphics file formats[J]. Sebastopol: O'Reilly,| c1996, 2nd ed., 1996, 1.

---

# References (cont.)

- Taubman D, Marcellin M. JPEG2000 Image Compression Fundamentals, Standards and Practice: Image Compression Fundamentals, Standards and Practice[M]. Springer Science & Business Media, 2012.
- Chang F, Dean J, Ghemawat S, Hsieh W C, Wallach D A, Burrows M, Chandra T, Fikkes A and Gruber R E: Bigtable: A Distributed Storage System for Structured Data. ACM Transactions on Computer Systems (TOCS), 26(2): 4, 2008
- Haghighat M, Zonouz S and Abdel-Mottaleb M: CloudID: Trustworthy Cloud-based and Cross-Enterprise Biometric Identification. Expert Systems with Applications, 42(21): 7905–7916, 2015
- Jiang X, Wang W, Sun T, et al. Detection of double compression in MPEG-4 videos based on Markov statistics[J]. Signal Processing Letters, IEEE, 2013, 20(5): 447-450.
- Sullivan G.J., Ohm J.R., Han W.J., et al. Overview of the High Efficiency Video Coding (HEVC) Standard[J]. IEEE Transaction on Circuits and Systems for Video Technology, 2012, 22(12): 1649-1668

---

# References (cont.)

- Vernik G, Shulman-Peleg A, Dippl S, Formisano C, Jaeger M C, Kolodner E K and Villari A M: Data On-boarding in Federated Storage Clouds. Proceedings of the 2013 IEEE Sixth International Conference on Cloud Computing. IEEE Computer Society, 2013
- Wiegand T., Sullivan G. J., Bjøntegaard G.,et al. Overview of the H.264/AVC Video Coding Standard[J]. IEEE Transaction on Circuits and Systems for Video Technology, 2003, 13: 560-576.
- ITU-T. Draft recommendation H.263 video coding for narrow telecommunication channels at below 64kbps[R]. 1995
- The Ultimate Guide to 4K Ultra HD, Ultra HDTV Magazine, 2013
- Android Developer: Android Supported Media Formats, <http://developer.android.com/>
- AVS [S/OL]. <http://www.avs.org.cn/>
- IBM Knowledge Center, <http://www.ibm.com/support/knowledgecenter/>
- iOS Developer Library: Using Audio, <https://developer.apple.com/library/ios/>

---

# QQ Group

<img src="figs/QQ-Group.jpg" alt="QQ-Group" width="300">

## Chinese students :  Please join this QQ group

## International students :  Not need to join this QQ group

<!---
landslide file.md -i -m -o > file.html
landslide file.md -i -x tables -m -o > file.html
--->
