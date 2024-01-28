<a name=top><br>
  <p align=center>&nbsp;<a href="/README.md#top">home</a> ::
  <a href="/docs/syllabus.md#top">syllabus</a> ::
  <a href="https://docs.google.com/spreadsheets/d/16yxmklx4zvmfAHE7QocOQZZ4v4UxD5ktJHWMJEjBcMI/edit#gid=0">groups</a> ::
  <a href="/LICENSE.md#top">&copy;&nbsp;2024</a>, <a href="http:/timm.fyi">Tim Menzies</a><br>
  <a href="/README.md#top"><img width=600  
     src="/etc/img/ase24.png"></a></p>


# Recursive Random Projections

The motto on SMO might be, learn a little, find regions of doubt, try there.

The motto of RRP is "look before your leap".

RRP is a landscape analysis technique:
- for $y=f(x)$,
  - if $x$ is cheap to explore but $y$ is expensive
  - look for patters in the independernt $X$ variables
    - before exploring the $Y$s
  - e.g in the following picture, if $y$ is some vertical goal function, then the other
    two dimensions are the $x$ choices

For multi-goal-reasoning, it is useful to conisder things as two spaces, the $X$s and the $Y$s
(so $f$ is the magic that bridges $X$s to   $Y$s)

![](cy.png)

In $Y$ space, many algorithms work in _generations_, find the best fo far (pruning the rest) then designing the next generation solution from the Pareto frontier seen so far,
- **Definition:** The Pareto frontier is a set of solutions that represents the best trade-off   between all  the      objective functions

![](generations.png)

Landscape analytics generalizes a range of
algorithms from different fields:
-   When used on the 𝑋 shape, landscape analytics might be called “clustering”.
(2) When used on the 𝑋, 𝑌 shape, limited sampling might be called “semi-supervised learning”;
(3) Similarly, in a joint analysis of the 𝑋, 𝑌 shape, if we bias our “leaps” towards regions that (in
the past) had good 𝑌 scores, landscape analytics might be called “reinforcement learning”.
(4) And if we use landscape analytics to jointly explore the𝑊 , 𝑌 shapes, then this could be called
“hyperparameter optimization”


In a recent survey of landscape analytics methods, Malan [36] notes that the term “landscape” is
a generalization of Sewell’s 1932 concept of “fitness landscape” [65] which was first defined for
evolutionary biology. Malan reports no less than 33 “families” of landscape analytics methods. Most
of these methods tend to enumerate the whole landscape, before exploring it. This approach is seen
in many parts of the Table 3 summary of the Malan survey; e.g.:
(1) Methods that assume that evaluation is fast or cheap usually exploit that property to make
many samples across the landscape.
(2) Methods that assume knowledge of optima also assume that the search space has been
pre-explored (to find that best point).



Landscap analysis:
-  data mining/ optimization =  as a search across landscapes. 
-  Given many examples of $(𝑋1, 𝑌1), (𝑋2, 𝑌2), ..$ etc then a learner $𝐿$ seeks some model $f$ that knows where parts
of the 𝑋 landscape connect to particular parts of the 𝑌 landscape.
