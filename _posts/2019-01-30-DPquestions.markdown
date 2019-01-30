---
layout:     post
title:      "动态规划"
subtitle:   "最长回文子串"
date:       2018-04-27 
author:     "Yu"
header-img: "img/post-bg-2015.jpg"
tags:
    - 学习
---
## 动态规划

动态规划经常用来求解最优子结构和重叠子问题，例如我们对重叠子问题多会使用递归来实现，但是递归存在的问题是，会进行大量的重复计算，而动态规划通过将之前计算的结果保存下来，避免了不必要的重复计算，提高了效率。  

## Java代码分析 



```
public String longestPalindrome(String s) {
        int len = s.length();
        if(s == null || len == 0){
            return s;
        }
        String res = "";
        int max = 0;
        //创建一个行列均为字符串长度的二维数组，创建时默认初始化为false
        boolean[][] dp = new boolean[len][len];
        for(int j = 0; j < len; j++){
            for(int i = 0; i <= j; i++){//这里只考虑了i<=j的情况，因为i>j时均为false
//当i==j,j-i==1,j-i==2时，只要满足s.charAt(i) == s.charAt(j)就是回文字符串
//如果不是这样，还要判断当前回文字符串的子串是不是回文字符串，即dp[i + 1][j - 1])，这就是动 
//态规划思想
                dp[i][j] = s.charAt(i) == s.charAt(j) && (j - i <= 2 || dp[i + 1][j - 1]);
                if(dp[i][j]){//如果是回文字符串
                    if(j - i + 1 > max){//并且比之前的回文字符串要长，更新字符串长度，记录字符串
                        max = j - i + 1;
                        res = s.substring(i, j + 1);
                    }
                }
            }
        }
        return res;
    }
```

  



