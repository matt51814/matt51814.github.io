---
title: "Gradient Descent"
date: 2026-02-14 12:00:00 -100
categories: [Gradient Descent, Deep Learning]
tags: [Gradient Descent, Deep Learning, ML]
---

Gradient Descent is an optimisation algorithm that is widely used in Machine Learning and Deep Learning. I want to go through the different versions of Gradient Descent that are commonly used in Deep Learning and capture why some methods in particular have became go-tos.

Let's begin with vanilla Gradient Descent. The essence (if you pardon the pun) of this is we have a function that we want to minimise. 

Let's assume the function is differentiable and convex, that is, let's assume we can calculate the derivative of the function at any point and that a line drawn between any two points on it's graph lies on or above the graph. 

An example of a single variable function that satisfies these criteria would be $$f(x)=x^2$$
This is differentiable $\forall x \in R$ with $$f'(x) = 2x$$
and also convex as $$f''(x) = 2 \geq 0$$
We can use this function to demonstrate Gradient Descent.

The update equation:
$$x_{t+1} = x_{t} - \eta f'(x_t)$$

Shows how one would use gradient descent in order to approach the minimum value of a function. Given a random point $x_t$ and a learning rate $\eta$ one can use the information gained from calculating the derivative in order to traverse the function to it's minimum. 

$\eta$ here refers to the learning rate. This is the "step size" that controls how far in the direction of the derivative we would like to travel. This is a parameter we want to optimise as if it's too large, we overshoot; if it's too small we'll be here all day.

We can run the update rule for a fixed number of iterations or more typically we would have a tolerance where if the updated value $x_{t+1}$ doesn't sufficiently change from the previous value then we stop.

This is the purely calculus approach to gradient descent but let's look into how this applied in Deep Learning!
