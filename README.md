java c
Nonlinear Optimization 1, Fall 2024 - Midterm
Problem 1 - Tell me truth and tell me why (25 points)For each of the following claims, state whether it is true or false (2pts) provide a short proof or counterexample justifying your claim (3pts).  An insightful justification for a wrong true/false answer can still get you the latter 3pts.
(a) Every global minimizer x*  ∈ Rd  of an arbitrary function f : Rd  → R has ▽f(x* ) = 0. (b) For any function f : Rd → R and point ¯(x) ∈ Rd , proxf(¯(x)) is a singleton.
(c) For any twice continuously differentiable function f : Rd  → R, if x*  ∈ Rd  has ▽2f(x* ) ≥ 0 and ▽f(x* ) = 0, then x*  is a local minimizer off.
(d) Every convex function f : Rd → R that is bounded below has a global minimizer.
(e) For any convex f : Rd → R, positive scalar ρ > 0, and point ¯(x) ∈ Rd, if some point ¯(x)* ∈ Rd has ρ(¯(x) — ¯(x)* ) ∈ ∂f(¯(x)* ) then ¯(x)*  globally minimizes f(x) + 2/ρ||x — ¯(x)||2(2).
Problem 2 - Constraints with subgradients (20 points + 5 bonus points)
Consider a convex function f : Rd → R and a convex, closed, nonempty set C ⊆ Rd.  We are interested in solving

Assume that this problem has at least one solution x⋆ . Show that the following hold true.
(a) (5 points) The function f is M-Lipschitz if, and only if, for all x ∈ Rd and all g ∈ ∂f(x) we have  ∥g∥2   ≤ M.
(b) (5 points) Consider the projected subgradient descent method that updates

where projC (x) := arg min y∈C ∥y − x∥2  denotes the orthogonal projection onto the set C. Show that this update is equivalent to

(c) (5 points) Show that iff is M-Lipschitz, then, the iterates of projected subgradient descent satisfy

You can use the fact that orthogonal projections onto convex sets are 1-Lipschitz without proving it.
(d) (5 points) Propose a sequence of nonconstant stepsizes αk that ensures that for any T ≥ 0 we have
You can use the fact that  without proving it.  This rate is worst
that the one we proved in clase with a constant αk, but it keeps improving as T grows.(d) (5 points) (Bonus  question)  Show  that  orthogonal  projections onto  convex sets are  1-
Lipschitz and that .
Problem 3代 写Nonlinear Optimization 1, Fall 2024 - MidtermMatlab
代做程序编程语言 - LASSO optimality conditions (15 points)
For any matrix A ∈ Rm×n , vector b ∈ Rm, and scalar γ > 0, consider the LASSO optimization problem defined as

Prove that a point x*  is a global minimizer off if and only if every i = 1 . . . n has

where Ai  is the ith column of A.
Problem 4 - Improved nonconvex guarantees (20 points)
For a continuously differentiable function  f : Rd   → R,  consider  the  following “error  bound” condition: there exists µ > 0 such that

for any point x ∈ Rd.
(a) (5pts) Show that the error bound above holds for every µ-strongly convex f.
(b) (5pts) Give an example of anonconvex function f : R → R satisfying the error bound.
(c) (5pts) Improve our nonconvex gradient descent convergence rate from class to the following: For any f with L-Lipschitz gradient and satisfying the error bound above, the iterates xk+1 = xk− ∇f(xk)/L have

(d) (5pts) Suppose instead of this error bound, we had  ∥∇f(x)∥2  ≥ µ(f(x) − minx′  f(x′)). In turn, we still havelimk→∞f(xk) = minf(x). Derive a convergence rate bounding f(xk) − minx f(x). Hint: Recall the analysis of gradient descent for smooth convex functions, we used a recurrence on the reciprocal of the objective gap, 1/(f(xk) − minx f(x)).
Problem 5 - Faster gradient norm convergence rates (20 points)
We showed in class that after k > 0 steps, the accelerated gradient method for minimizing a convex function f : Rd → R with L-Lipschitz gradient has

where x*  is any minimizer off.
(a) (10pts) Prove that this yk  has gradient norm bounded by

for some constant C depending on L and ∥x0 − x* ∥2 . Hint: Descent lemma.
(b) (10pts) Consider the following combination of the accelerated method and gradient de- scent for minimizing a function f with L-Lipschitz gradient:  For a fixed number k > 0, first run k steps of the accelerated method from a given x0 .  Then using the final iterate of the accelerated method yk  as an initial point ¯(x)0 ← yk, run k steps of gradient descent ¯(x)i+1 =¯(x)i− ∇f(¯(x)i)/L.Show the improved guarantee that some ¯(x)i  with 0 ≤ i < k of this gradient descent run has

         
加QQ：99515681  WX：codinghelp  Email: 99515681@qq.com
