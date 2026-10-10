## The learning rate behaviour 

*this is made before writing any code*

Learning rate behaviour about gradient descent :- 

you see that weights are influenced by the below equation:- 

```
W<sub>new</sub> = W<sub>old</sub> - LR * dL/dW
```


### when you take a small learning rate 
the w gets update very slowly towards convergence, but the problem is that most of the time training is set such that we stop after a number of steps (or epochs if you have only one batch, but if you find such good hardware please hit me up, i need it) so well we do not reach convergence most of the time 

### when you take a larger learning rate 
there are 3 things that can happen here then 

one is that the steps we take are large enough that we keep bouncing around the same well , you see it never settles or converges it just keeps going , this means that each overshoot is same size as the last , very intresting. 
the other is that the step is large enough that we bounce out of the particular curves concave and move into some other locality this causes divergence 
and the other one is that it might actually converge cus each overshoot is smaller than the last

---
## notes 😛
this is why most of us have decided to switch to adaptive moment estimator or **adam** these days, 
not like that solves this problem but is way more stable and changes learning rates based on previous estimates and it also very prettily solves gradient noise, giving more prirority to the recent most gradients, something called first and second moments , smoothens it by a lot. Some people also use Reduce LR on plateau which is another intresting thing 

