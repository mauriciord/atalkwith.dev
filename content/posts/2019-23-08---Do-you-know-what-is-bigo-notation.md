---
title: Do you know what is Big O Notation?
date: "2019-08-23T22:40:32.169Z"
template: "post"
draft: false
slug: "/posts/do-you-know-what-is-bigo-notation/"
category: "Javascript"
tags:
  - "Javascript"
  - "Data Structures"
  - "Algorithms"
description: "Introduction to Big-O notations"
---

![](/media/2019-23-08---Do-you-know-what-is-bigo-notation/bigo-meme.png)

As we need to improve our abilities as software engineer, we need to stop abusing the power of the language we're using and start acting as an analyst for the effectiveness of an algorithm application. This post will explain the concept of **Big O Notation**, and how to analyze an implementation of an algorithm on time (execution time) and space (memory consumed).

# The number of inputs

Analyzing with the Big O Notation rides you to following question: "What happens with n approaches to the infinity?". In other words, it will tell you about the algorithm.

![]()

![](/media/2019-23-08---Do-you-know-what-is-bigo-notation/graph.png)

[https://images.app.goo.gl/UDf6DhkMH3hM5Xsw6](https://images.app.goo.gl/UDf6DhkMH3hM5Xsw6)

Time complexities examples

# Big-O Notation rules

Let's say that an algorithm's complexity as f(n):

- *n* - The number of inputs
- *f(n)space* - The additional memory
- f(n)time - The time needed

The goal of the analysis is calculate the efficiency of the algorithm by calculating *f(n),* but because of it difficulty, we can use the Big-O Notation rules for that.

The first, second, fourth and sixty need to be in your mind, because they are commonly used.

- **Sum:** If f(n) is *O(h(n))* and *g(n)* is *O(p(n))*, then *f(n)+g(n)* is *O(h(n)+p(n))*. It's the sum of two Big-O notations.
- **Product:** If *f(n)* is *O(h(n))* and *g(n)* is *O(p(n))*, then *f(n)g(n*) is *O(h(n)p(n))*. It's the multiplication of Big-O notations.
- **Log:** *log(nk)* is *O(log(n))* for any constant *k > 0*. With the log, constants within a log function are also ignored in Big-O notation.
- **Polynomial:** If *f(n)* is a polynomial of degree k, then *f(n)* is *O(nk)*. The polynomial time complexities have Big-O notation of the same polynomial degree.
- **Transitive:** If *f(n)* is *O(g(n))* and *g(n)* is *O(h(n))*, then *f(n)* is *O(h(n))*. The time complexity has the same Big-O notation.
- **Coefficient:** If *f(n*) is *O(g(n))*, then *kf(n)* is *O(g(n))*, for any constant *k > 0*.

# Examples

## sum - *O(n) = n*

    function s(n) {
    	var total = 0;
    	for (var i = 0; i < n; i++) {
    			total += 1;
    	}
    	for (var i = 0; i < 8 * n; i++) {
    			total += 1;
    	}
    	
    	return total;
    }

## product - *O(n)=n^2*

    function prod(n) {
    	var total = 0;
    	for (var i = 0; i < n; i++){
    		total += 1;
    		for (var i = 0; i < 6 * n; i++){
    			total += 1;
    		}
    	}
    
    	return total;
    }

## polynomial - *O(nˆk)*

    function poly(n) {
    	var total = 0;
    	for (var i = 0; i < n * n; i++) {
    		total += 1;
    	}
    
    	return total;
    }

## coefficient - *O(n)*

    function coef(n) {
    	var total = 0;
    	for (var i = 0; i < n; i++) {
    		total += 1;
    	}
    
    	return total;
    }

# Conclusion

This article was an initial idea about Big-O notation, then if you want to be an expert you need to study more about it. You can read about Data Structures in another languages , for instance.
