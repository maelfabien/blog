---
title: Handle Missing Values in Time Series
layout: post
tags: [statistics]
subtitle : "Time Series"
---

In this quick article, we will review the two basic techniques to handle missing values in Time Series. 

The two techniques are the following :
- take the last known value and make a "forward fill", i.e to fill the values with the last known value until a new value is met
- take the first known value after the missing values, and full the values backward

Both techniques can be illustrated this way :

![images](https://maelfabien.github.io/assets/images/ts2_11.jpg)

To perform a forward fill, run the following command on your data frame :

```python
df.ffill(axis = 0)
```

| value | date |
| 1991-07-01 | 3.526591 |
| 1991-08-01 | 3.180891 |
| 1991-09-01 | 3.252221 |

To perform a backward fill, run the following command on your data frame :

```python
df.bfill(axis = 0)
```
