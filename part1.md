#### 1.Probability density function (pdf)와 cumulative distribution function (cdf) 개념을 설명해 주세요.

이 질문에 답하기 위해서는 우선 **random variable** 에 대한 정의가 필요합니다.

> _definition) Consider a random experiment with a sample space C. A function ![X](https://tex.s2cms.ru/svg/X), which assigns to each element ![c\in C](https://tex.s2cms.ru/svg/c%5Cin%20C) one and only one number ![X(c) = x](https://tex.s2cms.ru/svg/X(c)%20%3D%20x), is called a **random variable**. The **space** or **range** of ![X](https://tex.s2cms.ru/svg/X) is the set of real number ![D = \{x : x = X(c), c\in C\}](https://tex.s2cms.ru/svg/D%20%3D%20%5C%7Bx%20%3A%20x%20%3D%20X(c)%2C%20c%5Cin%20C%5C%7D)._

샘플을 추출할 수 있는 공간 ![C](https://tex.s2cms.ru/svg/C)가 있고, 해당 공간의 원소 ![c](https://tex.s2cms.ru/svg/c)에 대하여 1 대 1 대응을 만족하고 치역이 어떤 수(보통은 ![\R](https://tex.s2cms.ru/svg/%5CR))인 함수를 **random variable**이라 정의합니다. 이 때, 치역인 ![D](https://tex.s2cms.ru/svg/D)는 우리가 분석시 관심을 두는 샘플 스페이스가 됩니다.

샘플 스페이스 ![D](https://tex.s2cms.ru/svg/D) 이외에도 함수 ![X](https://tex.s2cms.ru/svg/X)는 또 자체의 확률을 내재하는데요(어떤 원소 ![x\in D](https://tex.s2cms.ru/svg/x%5Cin%20D)가 뽑힐 확률), 이를 두고 ![X](https://tex.s2cms.ru/svg/X)의 **distribution**이라고 합니다.

다음으로 **cumulative distribution function**에 대한 정의를 살펴보도록 하겠습니다.

> _definition) Let X be a random variable. Then its **cumulative distribution function**(cdf) is defined by ![F_X(x)](https://tex.s2cms.ru/svg/F_X(x)), where_
>
> > ![F_X(x) = P_X((-\infty, x]) = P({c\in C : X(c) \leq x})](https://tex.s2cms.ru/svg/F_X(x)%20%3D%20P_X((-%5Cinfty%2C%20x%5D)%20%3D%20P(%7Bc%5Cin%20C%20%3A%20X(c)%20%5Cleq%20x%7D))

![X](https://tex.s2cms.ru/svg/X)를 **random variable**로 두고 그 치역을 들여다 보면, 해당 치역에서 의미를 부여할 수 있는 범위는 ![(-\infty, x]](https://tex.s2cms.ru/svg/(-%5Cinfty%2C%20x%5D) 즉 어떤 치역의 원소 ![x](https://tex.s2cms.ru/svg/x)이하의 원소 모두입니다. 이렇게 정의하면 축적된 확률분포를 알 수 있을 뿐만 아니라 분포의 *skewness* 또한 간접적으로 파악할 수 있는 장점이 있습니다.

그 외의 **cumulative distribution function**의 특성은 다음과 같습니다.

1.  *Monotone increasing*

    For all ![a](https://tex.s2cms.ru/svg/a) and ![b](https://tex.s2cms.ru/svg/b), if ![a < b](https://tex.s2cms.ru/svg/a%20%3C%20b), then ![F(a) \leq F(b)](https://tex.s2cms.ru/svg/F(a)%20%5Cleq%20F(b))

2.  *The lower limit of ![F](https://tex.s2cms.ru/svg/F) is 0*  
    ![\lim_{x\to-\infty} F(x) = 0](https://tex.s2cms.ru/svg/%5Clim_%7Bx%5Cto-%5Cinfty%7D%20F(x)%20%3D%200)

3.  *The upper limit of ![F](https://tex.s2cms.ru/svg/F) is 1*  
    ![\lim_{x\to\infty} F(x) = 1](https://tex.s2cms.ru/svg/%5Clim_%7Bx%5Cto%5Cinfty%7D%20F(x)%20%3D%201)

4.  *F is right continuous*  
    ![\lim_{x\leftarrow x_0} F(x) = f(x_0)](https://tex.s2cms.ru/svg/%5Clim_%7Bx%5Cleftarrow%20x_0%7D%20F(x)%20%3D%20f(x_0))


마지막으로 **probability density function** 의 정의를 살펴보겠습니다. 살펴보기 이전에 우리는 **continuous random variable**에 대한 정의가 필요합니다.

> *definition) We say a random variable is a **continuous random variable** if its cumulative distribution function ![F_X(x)](https://tex.s2cms.ru/svg/F_X(x)) is a continuous function for all ![x\in \R](https://tex.s2cms.ru/svg/x%5Cin%20%5CR)*

즉 *cdf* 가 연속인 *random variable*을 두고 우리는 **continuous random variable**이라고 정의합니다. 대부분의 *continuous random variable*들은 절대 연속입니다. 이것의 해석적인 정의는 다음과 같습니다.

> *definition) Let ![I](https://tex.s2cms.ru/svg/I) be an interval in the real line ![\R](https://tex.s2cms.ru/svg/%5CR). A function ![f:I\rightarrow \R](https://tex.s2cms.ru/svg/f%3AI%5Crightarrow%20%5CR) is absolutely continuous on ![I](https://tex.s2cms.ru/svg/I) if for every positive number ![\epsilon](https://tex.s2cms.ru/svg/%5Cepsilon), there is a positive number ![\delta](https://tex.s2cms.ru/svg/%5Cdelta) such that whenever a finite sequence of pairwise disjoint sub-intervals ![(x_k, y_k)](https://tex.s2cms.ru/svg/(x_k%2C%20y_k)) of ![I](https://tex.s2cms.ru/svg/I) with ![x_k, y_k \in I](https://tex.s2cms.ru/svg/x_k%2C%20y_k%20%5Cin%20I) satisfies ![\sum_{k} (y_k - x_k) < \delta](https://tex.s2cms.ru/svg/%5Csum_%7Bk%7D%20(y_k%20-%20x_k)%20%3C%20%5Cdelta) then ![\sum_{k} |f(y_k) - f(x_k)| < \epsilon](https://tex.s2cms.ru/svg/%5Csum_%7Bk%7D%20%7Cf(y_k)%20-%20f(x_k)%7C%20%3C%20%5Cepsilon)*

즉 어떠한 정의역의 서로소인 원소들의 차로 급수를 형성하더라도, 그 원소들의 치역의 원소들의 차의 절댓값의 급수는 일정 범위를 넘지 않는다는 정의입니다. 이것과 동치인 정의는 다음과 같습니다.

> *definition) ![f](https://tex.s2cms.ru/svg/f) has derivative ![f^\prime](https://tex.s2cms.ru/svg/f%5E%5Cprime) a.e., the derivative is Lebesgue integrable, and ![f(x) = f(a) + \int_{a}^{x} f^\prime(x) dx](https://tex.s2cms.ru/svg/f(x)%20%3D%20f(a)%20%2B%20%5Cint_%7Ba%7D%5E%7Bx%7D%20f%5E%5Cprime(x)%20dx) for all ![x\in [a, b]](https://tex.s2cms.ru/svg/x%5Cin%20%5Ba%2C%20b%5D)*

즉 ![f](https://tex.s2cms.ru/svg/f) 가 measure zero set 이외의 공간에서 도함수를 가지고, 도함수가 르벡 적분 가능하며 위의 식과 같이 표현가능할 경우 절대연속이라 정의합니다. 이것을 *continuous random variable*에 적용하게 되면,

![F_X(x) = f(-\infty) + \int_{-\infty}^{x} f_X(t) dt](https://tex.s2cms.ru/svg/F_X(x)%20%3D%20f(-%5Cinfty)%20%2B%20%5Cint_%7B-%5Cinfty%7D%5E%7Bx%7D%20f_X(t)%20dt)

이고 ![f(-\infty) = 0](https://tex.s2cms.ru/svg/f(-%5Cinfty)%20%3D%200)이므로

![F_X(x) = \int_{-\infty}^{x} f_X(t) dt](https://tex.s2cms.ru/svg/F_X(x)%20%3D%20%5Cint_%7B-%5Cinfty%7D%5E%7Bx%7D%20f_X(t)%20dt)

입니다. 이때 ![f_X(t)](https://tex.s2cms.ru/svg/f_X(t))를 **probability density function**이라 정의합니다.
