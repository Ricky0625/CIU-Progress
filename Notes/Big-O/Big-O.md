# Algorithmic complexity / Big-O / Asymptotic analysis

==Learning Outcome / Expectation==

- Don't need to understand all the math behind it.
- Need to understand how to express the complexity of an algorithm in terms of `Big-O`.

---

## Asymptotic Notation

Material: [CS50 - Asymptotic Notation][https://youtu.be/iOq5kSKqeR4]

> What does it mean when we are talking about **fast** and **efficient** algorithm?

It is not about taking the real-time measurement like *minutes* or *seconds* to measure because in computers, there are factors that will affect the value of the measurement. For example, maybe my operating system is older than yours, which makes my program runs slower. Or perhaps I'm playing an online game while running the program. The online game consumes too much of my memory which makes my program slow. 

So as you can see calculating the runtimes of programs is not a proper way to determine it's fast or efficient. Then how should we compare it regardless their hardware or software environment?

That's why the **Big-O Notation** was devised for measuring the asymptotic complexity of a program. Big-O notation is also known as **Asymptotic Notation**.

> #### *Asymptotic* ~adjective~
>
> A straight line associated with a curve such that as a point moves along an infinite branch of the curve the distance from the point to the line approaches zero and the slope of the curve at the point approaches the slope of the line

### How to describe an algorithm using Big-O

- Analyze how fast a program's runtime grows asymptotically.
- For example, sorting an array of size 1000 compared to an array of size 10. How does the runtime of your program grow?

**Count the number of `char` of a string**

```
"cat"
 123
```

Idea is when the program encounters a character, `counter++`. So, we can say this algorithm is said to run in linear time because as ==the number of `char` increased==, the ==time to traverse through the string will increase== as well. In short, it runs in:

<p style="font-size: 24px; text-align: center; font-family: Times New Roman">O(n)</p>

**Accessing an index of an array**

```C
int arr[5] = {1, 2, 3, 4, 5};
printf("%d", arr[1]);
```

Something like this, when we express it in terms of `Big-O`, it runs in:

<p style="font-size: 24px; text-align: center; font-family: Times New Roman">O(1)</p>

This is also known as **Constant Time**. Constant time doesn't have to mean that your program runs in one step, but no matter how many steps it is, if it doesn't change with the size of the inputs, it's still asymptotically constant which we represent as O(1).

There are many kinds of Big-O runtimes to measure algorithms with.

[Big-O Algorithm Complexity Cheat Sheet](https://www.bigocheatsheet.com/)

1. O(n)

2. O(1)

3. O(n^2^) - as the `n` grows, the time to run will increase. Similar to O(n) but this takes more time.

4. O(log n) -as the `n` grows, the time to run the program will **slowly** increase

   ...and many more

> ##### Keynote
>
> Let's say there are two algorithms. One runs in O(n), another runs in O(n^2^). Does it means that O(n^2^) will always worse than O(n)?
>
> Not exactly! Maybe the O(n^2^) algorithm might actually work faster than O(n) in some cases!
>
> But, as the input size increases, the O(n^2^) algorithm's runtime will eventually eclipse the runtime of O(n) algorithm, as described as the image below.

![image-20220314213318851](C:\Users\Asus\AppData\Roaming\Typora\typora-user-images\image-20220314213318851.png)
