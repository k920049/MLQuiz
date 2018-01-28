#### 3\. Prior, likelihood, posterior에 대해 각각 설명해 주세요

#### Prior

*X*가 ![\theta](https://tex.s2cms.ru/svg/%5Ctheta)에 의해 그 분포가 결정되는 *random variable* 이라고 가정하고, 이 때 ![\theta](https://tex.s2cms.ru/svg/%5Ctheta)는 *well-defined* 된 *set* ![\Omega](https://tex.s2cms.ru/svg/%5COmega) 의 한 원소라고 가정합니다. 여기서 ![\theta](https://tex.s2cms.ru/svg/%5Ctheta) 는 평균이나 분산 같은 추정량이면 데이터를 더 잘 표현할 수 있는 값이 됩니다.

역사적으로 *Frequentist*들은 이 ![\theta](https://tex.s2cms.ru/svg/%5Ctheta)를 파라미터로 보았지만, *Bayesian*들은 ![\theta](https://tex.s2cms.ru/svg/%5Ctheta)를 ![\Omega](https://tex.s2cms.ru/svg/%5COmega)를 정의역으로 가지는 *random variable* ![\Theta](https://tex.s2cms.ru/svg/%5CTheta)라는 관점에서 보았습니다. 그러므로 우리는 ![\Theta](https://tex.s2cms.ru/svg/%5CTheta)에 관한 *pdf*를 정의할 수 있고,

![h(\theta) = \begin{cases}k, \theta\in\Theta\\ 0, \theta\notin\Theta\end](https://tex.s2cms.ru/svg/h(%5Ctheta)%20%3D%20%5Cbegin%7Bcases%7Dk%2C%20%5Ctheta%5Cin%5CTheta%5C%5C%200%2C%20%5Ctheta%5Cnotin%5CTheta%5Cend)

이 *pdf*를 **prior** 라고 정의합니다.

#### Likelihood

*Random sample* ![X_1, X_2, ... X_n](https://tex.s2cms.ru/svg/X_1%2C%20X_2%2C%20...%20X_n) 이 있다고 가정합니다. ![\Theta = \theta](https://tex.s2cms.ru/svg/%5CTheta%20%3D%20%5Ctheta)가 결정되었을 때 우리는 이것을 *joint conditional pdf*의 형태로 나태낼 수 있고 그것은 다음과 같습니다.

![L(x|\theta) = f(x_1|\theta)...f(x_n|\theta)](https://tex.s2cms.ru/svg/L(x%7C%5Ctheta)%20%3D%20f(x_1%7C%5Ctheta)...f(x_n%7C%5Ctheta))

우리는 이것을 **likelihood** 라고 정의합니다.

#### Posterior

위의 식에 **Bayes theorem**을 적용하게 되면

![g(x, \theta) = L(x|\theta)h(\theta)](https://tex.s2cms.ru/svg/g(x%2C%20%5Ctheta)%20%3D%20L(x%7C%5Ctheta)h(%5Ctheta))

가 되고 이것을 ![\theta](https://tex.s2cms.ru/svg/%5Ctheta) 에 관해서 marginalize out 시키면

![g_1(x) = \int_{-\infty}^{\infty} g(x, \theta)d\theta](https://tex.s2cms.ru/svg/g_1(x)%20%3D%20%5Cint_%7B-%5Cinfty%7D%5E%7B%5Cinfty%7D%20g(x%2C%20%5Ctheta)d%5Ctheta)

가 성립합니다. 이것을 *random sample* ![X](https://tex.s2cms.ru/svg/X) 가 주어졌을 때 ![\Theta](https://tex.s2cms.ru/svg/%5CTheta)에 관한 *pdf* 로 나타내면

![k(\theta|x) = \frac{g(x, \theta)}{g_1(x)} = \frac{L(x|\theta)h(\theta)}{g_1(x)}](https://tex.s2cms.ru/svg/k(%5Ctheta%7Cx)%20%3D%20%5Cfrac%7Bg(x%2C%20%5Ctheta)%7D%7Bg_1(x)%7D%20%3D%20%5Cfrac%7BL(x%7C%5Ctheta)h(%5Ctheta)%7D%7Bg_1(x)%7D)

입니다. 이 때 ![k(\theta|x)](https://tex.s2cms.ru/svg/k(%5Ctheta%7Cx)) 를 **posterior** 라 정의합니다.
