## 4.2 Mean Value Theorem

*Rolle's Theorem states that*
```
the function f must be continous on [a,b]
and be differentiable on (a,b)

if f(a)=f(b) exists
then f'(c)=0
```

![[Pasted image 20231118142554.png]]

*The Mean Value Theorem states*

```
the function f must be continous on [a,b]
and be differentiable on (a,b)

then
f'(c) = f(b)-f(a)/b-a
f'(c) = the slope of the tangent line.
f(b)-f(a)/b-a = the slope of the secant line.

Basically there is a point where the slope of the tangent line is equal to the slope of the secant line.

Secant line touches 2 specific points, in this case a and b.
Tangent line touches a point that touches only 1 point.

So basically there IS a point where the slope of the tangent line is equal to the slope of the secant line.
f'(c) ofc is the same thing as rolle's theorem where it equals to a critical point. 

In the example of y=x^2 on the interval [1,3],
the function and interval supports all mean value theorem requirements,
and therefore
f'(c) is just the derivative with c replaced. Therefore in the end you are just solving for the unknown c, which is the point where the instantaneous rate of change of f(x)=x^2is equal to the average rate of change over [1,3], and in this case, c=2c=2.
```

## 4.4 Indeterminate Forms & L'Hopital Rule

Lets say we want to find the following limit

$$ \lim_{x \to a} \frac{f(x)}{g(x)}$$
Lets say that limit is in the form of either 0/0 or infinity/infinity. These are known as indeterminate forms. If that is the case, then the limit is equal to the following limit:
$$\lim_{x \to a}\frac{f'(x)}{g'(x)}$$
Lets say we wanna find the limit of
$$ \large\lim_{x \to \infty} \frac{e^x}{x^2}$$
Welp, e^infinity is just infinity, and infinity squared is just infinity so we do in fact have an indeterminate form.

Well, we just derive now.
$$\frac{d}{dx} e^x = e^x \space  \space \frac{d}{dx} x^2 = 2x $$
$$ \lim_{x \to \infty} \frac{e^x}{2x} $$
We still run into an issue, its still infinity/infinity.

$$\frac{d}{dx} e^x = e^x \space \space \frac{d}{dx} 2x = 2 $$
$$ \lim_{x \to \infty} \frac{e^x}{2} $$
Well this is much better, this just equals infinity rather than a fraction, and that is a valid limit.
$$ \LARGE \infty$$

## 4.7 Optimization Problems

1. Read CAREFULLY
2. Maybe draw the situation
3. Formulate an objective function; which represents the quantity you need to optimize, so like area or volume or perimeter or money
4. Identify the constraints
5. Express the objective function in terms of 1 variable.
6. Find the critical points of that one variable function.
7. Interpret your results and find the answer

Say in this example; 
```
Find two numbers whose sum is 60 and whose product is maximum.
First I'd setup 2 equations, the sum and product.
S = x + y P = xy
60 = x+y
Clearly, the constraint equation is the Sum and the Objective is the product.
Solving for y
60-x=y
Therefore, P = (60-x)(x)
P = 60x-x^2
deriving dP/dx 0=60-2x
x=30
y therefore must equal 30.
P = 900
```

## 4.9 Anti-derivatives

Not much to say here, just follow the rules below.

![[Pasted image 20231118184151.png]]

## 5.1 The area and distance Problems

Basically rectangles and stuff
With the equation y=x^2 we wanna find the area of the region between x = 0 and x = 1
We will be using right endpoints , so 0 1/4, 1/4 1/2, 1/2 3/4, 3/4 1. The height of a rectangle is determined by inputting the right endpoint, so say 1/4 into the function to get 1/16. So the first rectangle is 1/4 by 1/16. We can manually calculate this to be the base times height of 1 rectangle + bh of another. After calculating all the values we end up with;
$$ R_4 = \frac{15}{32} = 0.46875 $$
The four right endpoints rectangles is equal to 15/32. Right endpoints will always over estimate the area. So in our case so far we know that;
$$ A < 0.46875 $$
We can also use smaller rectangles, which will be left endpoints. If we use left endpoints, we first run into 1 issue, that is the height of the first rectangle will be 0 and therefore the area of the first rectangle will be 0, since we use left endpoints and 0 is the starting y value. The rectangles will have the same base as the right ones but different height since different endpoint. The first rectangle is equal to 0 area, second one is 1/64, third one is 1/16, and fourth one is 9/64. Adding all these together we get 14/64 or 7/32. 
$$ L_4 = \frac{7}{32} = 0.21875 $$
Therefore: $$ 0.21875 < A < 0.46875 $$
The more rectangles we use the more exact of an answer we can get.
After using a computer we can see that the area of the selected region slowly approaches 1/3
$$ \lim_{n \to \infty} R_n = \frac{1}{3} $$
$$ \large\text{So here we have an idea of } R_n \text{, whose rectangles are of the width } \frac{1}{n} \text{ and the heights} $$
$$ \large\text{ at values of the function } f(x) = x^2 \text{ at the points 1/n 2/n 3/n... } \frac{n}{n} $$
The heights therefore are $$ (\frac{n}{n})^2 $$ Thus;
$$ R_n = \frac{1}{n} f(\frac{n}{n}) $$
Where f(n/n) in our case is (n/n) squared since function is x^2.

$$ \frac{n(n+1)(2n+1)}{6} $$
Thus;
$$ R_n = \frac{1}{n^3} \cdot  \frac{n(n+1)(2n+1)}{6}  =  \frac{(n+1)(2n+1)}{6n^2}  $$
Thus we have the limit;
$$ \lim_{n \to \infty} R_n = \lim_{n \to \infty}  \frac{(n+1)(2n+1)}{6n^2} $$
Once we plugin our values, we have proved that the area is truly equal to 1/3.

Say we have a function f(x) and want to find arbitrary area A which will be defined as the region S. So first of all there is an interval between the 2 points we wish to compute, they will be points *a* and *b*. The width of the interval [a,b] is b-a (they are points on the x axis) so the width of each of the *n* strips will be 
$$ \Delta x = \frac{b-a}{n} $$
These strips divide the interval [a,b] into *n* subintervals. 
$$ [x_0, x_1], \space [x_{n-1}, x_n] $$
where x_0 = a and x_n = b. The right endpoints of our subintervals go:
$$ x_i = a + i\Delta x $$
Lets approximate the *i*th strip Si by a rectangle with width of delta x and height f(xi) which is the value of f at the right endpoint. The area is f(xi)deltax. Basically:
$$ R_n = f(x_n)\Delta x $$
As n approaches infinity, the approximation gets better and better till its, correct. We can write this in limit form.
$$ A = \lim_{n \to \infty} R_n = \lim_{n \to \infty} f(x_n)\Delta x $$
Same proof but using left endpoints:
$$ L_n = A = \lim_{n \to \infty} f(x_{n-1})\Delta x $$
![[Pasted image 20231119184204.png]]

A is the area that is smaller than the upper sums and larger than the lower sums. 
![[Pasted image 20231119184526.png]]

From now on we will use sigma notation to denote these sums more compactly.
![[Pasted image 20231119184751.png]]

This stuff is pretty complicated and all theory, so lets run another example.

Let *A* be the area of the region underneath the graph of f(x)=e^-x between 0 and 2
a) Using right endpoints find an expression for A as a limit. Do not evaluate the limit.
b) estimate the area by taking the sample points to be midpoints and using 4 subintervals and then 10 subintervals.

(a) since a = 0 and b = 2 the width of a sub interval is 
$$ \Delta x = \frac{2-0}{n} $$
Therefore we have 2i/n
$$ x_n = 2n/n $$
$$ R_n = f(x_n)\Delta x $$
Which in our case is 
$$ R_n = e^{-x_n} \Delta x $$
$$ e^{\frac{-2n}{n}}(\frac{2}{n}) $$
Therefore we can write the area as:
![[Pasted image 20231119192801.png]]
![[Pasted image 20231119192818.png]]
![[Pasted image 20231119193823.png]]

 Velocity Problems / Distance Problems

Distance = Velocity * Time
Seems simple, right? But what if the velocity varies?
Suppose we have a car, with the following statistics:
![[Pasted image 20231120083824.png]]
![[Pasted image 20231120083833.png]]
During the first 5 seconds, the velocity doesnt change much, so lets say the velocity was 25 ft/s over 5 seconds so 125 feet traveled. We can repeat this ideology for every time interval. Clearly a limit or summation can be used here.

In general, suppose an object moves with velocity v = f(t), where a<=t<=b and f(t) >= 0. In velocity problems, delta X is equal to (b-a)/n. A summation for this goes as follows:

$$ \LARGE\sum^{n}_{i=1} f(t_{i-1})\Delta t $$

Thats if we use left endpoints. If we use right endpoints;
$$ \LARGE\sum^{n}_{i=1} f(t_i)\Delta t $$
Both will give you the same exact value.

The more frequent we calculate the velocity the better our estimates become, therefore we can write a limit for this:

$$ \LARGE d = \lim_{n \to \infty} \sum^{n}_{i=1} f(t_{i-1}) \Delta t = \lim_{n \to \infty} \sum^{n}_{i=1} f(t_i)\Delta t $$
## 5.2 The Definite Integral

Alright so the Definite integral is basically the same as that limit from earlier:

![[Pasted image 20231120103254.png]]
It is basically:
$$ \LARGE\int^{b}_{a}f(x)dx=\lim_{n \to \infty}\sum^{n}_{i=1}f(x_i^*)\Delta x $$
![[Pasted image 20231120103718.png]]
![[Pasted image 20231120104527.png]]

Heres an example:
Evaluate the Riemann sum for f(x) = x^3 - 6x 0<= x <= 3 with n=6 subintervlas

So with n=6 subintervals the interval width is delta X = (3-0)/6 equaling 1/2 and so the right endpoints are:
x1 = 0.5 x2 =1.0 x3= 1.5 x4 = 2.0 x5 = 2.5 x6=3.0
So the riemann sum is:
$$ \LARGE R_6 = \sum^{6}_{i=1}f(x_i)\Delta x $$
![[Pasted image 20231120112855.png]]
![[Pasted image 20231120112936.png]]
The answer here is going to be negative since the area of negative is greater than the area of positive.![[Pasted image 20231120114749.png]]
![[Pasted image 20231120114756.png]]
![[Pasted image 20231120123415.png]]

`To find the limit representing the area under the graph of sqrtx​ from 1 to 4, you can set up a Riemann sum as the limit of a sum. The Riemann sum involves partitioning the interval [1,4]into n subintervals, with each subinterval's width (ΔxΔx) determined by 4−1nn4−1​. The sample point ci within each subinterval is commonly chosen as the right endpoint, resulting in ci=xi=1+i⋅4−1/n. The limit as n approaches infinity of the Riemann sum corresponds to the definite integral of sqrtx​ from 1 to 4. In simpler terms, this limit represents the area under the curve sqrtx from 1 to 4 on the x-axis.
`
![[Pasted image 20231120123629.png]]
![[Pasted image 20231120123637.png]]
![[Pasted image 20231120125416.png]]
![[Pasted image 20231120125642.png]]
Basically you get the midpoint of each interval so say that our delta x is 2 then we use the calculuation every 1 point so say on interval 0 to 10 we have 5 rectangles, our midpoints would be 1 3 5 7 9
Though a better way would just be the indefinte integral...
![[Pasted image 20231120125700.png]]
![[Pasted image 20231120125740.png]]
![[Pasted image 20231120125759.png]]
![[Pasted image 20231120125837.png]]
![[Pasted image 20231120125843.png]]
![[Pasted image 20231120130048.png]]
![[Pasted image 20231120130110.png]]
![[Pasted image 20231120130159.png]]


## 5.4 Indefinite Integrals
![[Pasted image 20231120131313.png]]
![[Pasted image 20231120131320.png]]
![[Pasted image 20231120131342.png]]
![[Pasted image 20231120132034.png]]
![[Pasted image 20231120133352.png]]

____