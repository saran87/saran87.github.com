---
layout: post
title: "Union-Find Data Structure Python : For clustering algorithm"
date: 2013-01-04 22:45
comments: true
categories: [Python, Kruskal's algorithm, Union-Find, Clustering]
---
I was coding kurskal’s clustering algorithm for a max-spacing k-clustering problem. To improve the efficiency of the clustering algorithm, I needed an efficient data structure to union two cluster and find an element in a cluster.

Union Find (disjoint-set) data structure is best option for above operations. Implemented the Union Find structure as per the algorithm specified in the Introduction to Algorithms book.

This Implementation includes Union by Rank and Path compression, which gives a amortized runtime of a(n) (i.e a - <a href="http://en.wikipedia.org/wiki/Ackermann_function" title="Ackermann function">Ackermann function</a>)

{% gist 4751455 %}
