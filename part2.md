#### 2.가우시안 분포에 대해 설명해 주세요

다음과 같은 적분을 고려해 보겠습니다.

![I = \int_{-\infty}^{\infty}\frac{1}{\sqrt{2\pi}}exp(\frac{-z^2}{2})dz -(1)](https://tex.s2cms.ru/svg/I%20%3D%20%5Cint_%7B-%5Cinfty%7D%5E%7B%5Cinfty%7D%5Cfrac%7B1%7D%7B%5Csqrt%7B2%5Cpi%7D%7Dexp(%5Cfrac%7B-z%5E2%7D%7B2%7D)dz%20-(1))

이 적분의 integrand 는 positive continuous function 이며 upper bound 가 존재합니다.

![0 < exp(\frac{-z^2}{2}) < exp(-|Z| + 1), -\infty < z < \infty](https://tex.s2cms.ru/svg/0%20%3C%20exp(%5Cfrac%7B-z%5E2%7D%7B2%7D)%20%3C%20exp(-%7CZ%7C%20%2B%201)%2C%20-%5Cinfty%20%3C%20z%20%3C%20%5Cinfty)

이 적분의 값을 구하기 위해 우선 제곱을 씌워주면

![I^2 = \frac{1}{\sqrt{2\pi}}\int_{-\infty}^{\infty}\int_{-\infty}^{\infty}exp(-\frac{z^2 + w^2}{2})dzdw](https://tex.s2cms.ru/svg/I%5E2%20%3D%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%5Cpi%7D%7D%5Cint_%7B-%5Cinfty%7D%5E%7B%5Cinfty%7D%5Cint_%7B-%5Cinfty%7D%5E%7B%5Cinfty%7Dexp(-%5Cfrac%7Bz%5E2%20%2B%20w%5E2%7D%7B2%7D)dzdw)

가 됩니다. 이것을 극좌표계로 다시 표현하면

![I^2 = \frac{1}{\sqrt{2\pi}}\int_{0}^{2\pi}\int_{0}^{\infty}exp(-\frac{r^2}{2})r drd\theta = \frac{1}{\sqrt{2\pi}}\int_{0}^{2\pi}d\theta = 1](https://tex.s2cms.ru/svg/I%5E2%20%3D%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%5Cpi%7D%7D%5Cint_%7B0%7D%5E%7B2%5Cpi%7D%5Cint_%7B0%7D%5E%7B%5Cinfty%7Dexp(-%5Cfrac%7Br%5E2%7D%7B2%7D)r%20drd%5Ctheta%20%3D%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%5Cpi%7D%7D%5Cint_%7B0%7D%5E%7B2%5Cpi%7Dd%5Ctheta%20%3D%201)

입니다.

(1) 에서 *integrand*는 모든 정의역에 대해서 양의 값(support)을 가지고, 적분하면 1이 되므로 *continuous random variable*의 *pdf*가 됩니다. 우리는 이 ![Z](https://tex.s2cms.ru/svg/Z)에 관한 분포를 **Normal(Gaussian) distribution**이라 정의하고 다음과 같이 표현합니다.

![f(z) = \frac{1}{\sqrt{2\pi}}exp(\frac{-z^2}{2}), -\infty < z < \infty](https://tex.s2cms.ru/svg/f(z)%20%3D%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%5Cpi%7D%7Dexp(%5Cfrac%7B-z%5E2%7D%7B2%7D)%2C%20-%5Cinfty%20%3C%20z%20%3C%20%5Cinfty)

이 분포의 *moment generating function*은 다음과 같습니다. 우선 ![t\in \R](https://tex.s2cms.ru/svg/t%5Cin%20%5CR)에서

![E[exp(tZ)] = \int_{-\infty}^{\infty}exp\{tz\}\frac{1}{\sqrt{2\pi}}exp\{-\frac{1}{2}z^2\}dz](https://tex.s2cms.ru/svg/E%5Bexp(tZ)%5D%20%3D%20%5Cint_%7B-%5Cinfty%7D%5E%7B%5Cinfty%7Dexp%5C%7Btz%5C%7D%5Cfrac%7B1%7D%7B%5Csqrt%7B2%5Cpi%7D%7Dexp%5C%7B-%5Cfrac%7B1%7D%7B2%7Dz%5E2%5C%7Ddz)

![ = exp\{\frac{1}{2}t^2\}\int_{-\infty}^{\infty} \frac{1}{\sqrt{2\pi}}exp\{-\frac{1}{2}(z - t)^2\}dz](https://tex.s2cms.ru/svg/%20%3D%20exp%5C%7B%5Cfrac%7B1%7D%7B2%7Dt%5E2%5C%7D%5Cint_%7B-%5Cinfty%7D%5E%7B%5Cinfty%7D%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%5Cpi%7D%7Dexp%5C%7B-%5Cfrac%7B1%7D%7B2%7D(z%20-%20t)%5E2%5C%7Ddz)

![ = exp\{\frac{1}{2}t^2\}\int_{-\infty}^{\infty} \frac{1}{\sqrt{2\pi}}exp\{-\frac{1}{2}w^2\}dw](https://tex.s2cms.ru/svg/%20%3D%20exp%5C%7B%5Cfrac%7B1%7D%7B2%7Dt%5E2%5C%7D%5Cint_%7B-%5Cinfty%7D%5E%7B%5Cinfty%7D%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%5Cpi%7D%7Dexp%5C%7B-%5Cfrac%7B1%7D%7B2%7Dw%5E2%5C%7Ddw)

입니다. 따라서

![M_Z(t) = exp\{\frac{1}{2}t^2\}](https://tex.s2cms.ru/svg/M_Z(t)%20%3D%20exp%5C%7B%5Cfrac%7B1%7D%7B2%7Dt%5E2%5C%7D)

이고, 이것의 1 계 도함수와 2 계 도함수는 다음과 같습니다.

![M_z^\prime(t) = t*exp\{\frac{1}{2}t^2\}](https://tex.s2cms.ru/svg/M_z%5E%5Cprime(t)%20%3D%20t*exp%5C%7B%5Cfrac%7B1%7D%7B2%7Dt%5E2%5C%7D)

![M_z^{\prime\prime}(t) = exp\{\frac{1}{2}t^2\} + t^2*exp\{\frac{1}{2}t^2\}](https://tex.s2cms.ru/svg/M_z%5E%7B%5Cprime%5Cprime%7D(t)%20%3D%20exp%5C%7B%5Cfrac%7B1%7D%7B2%7Dt%5E2%5C%7D%20%2B%20t%5E2*exp%5C%7B%5Cfrac%7B1%7D%7B2%7Dt%5E2%5C%7D)

입니다. ![t = 0](https://tex.s2cms.ru/svg/t%20%3D%200)에서 값을 평가하면

![E(Z) = 0, Var(Z) = 1](https://tex.s2cms.ru/svg/E(Z)%20%3D%200%2C%20Var(Z)%20%3D%201)

입니다.

다음으로 임의의 *continuous random variable* ![X](https://tex.s2cms.ru/svg/X)를 다음과 같이 정의합니다.

![X = bZ + a, b > 0](https://tex.s2cms.ru/svg/X%20%3D%20bZ%20%2B%20a%2C%20b%20%3E%200)

이것은 *bijective*하므로 *(jacobian)* ![J = b^{-1}](https://tex.s2cms.ru/svg/J%20%3D%20b%5E%7B-1%7D)이고 이것을 변수변환하면 *pdf*는 다음과 같은 형태가 됩니다.

![f_X(x) = \frac{1}{\sqrt{2\pi}b}exp\{-\frac{1}{2}(\frac{x - a}{b})^2\}, -\infty < x < \infty](https://tex.s2cms.ru/svg/f_X(x)%20%3D%20%5Cfrac%7B1%7D%7B%5Csqrt%7B2%5Cpi%7Db%7Dexp%5C%7B-%5Cfrac%7B1%7D%7B2%7D(%5Cfrac%7Bx%20-%20a%7D%7Bb%7D)%5E2%5C%7D%2C%20-%5Cinfty%20%3C%20x%20%3C%20%5Cinfty)

이것이 일반적으로 정의되는 Gaussian 분포함수의 형태입니다.
