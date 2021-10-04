### ✨문제

Write a function that reverses a string. The input string is given as an array of characters `s`.

**Example 1:**

```
Input: s = ["h","e","l","l","o"]
Output: ["o","l","l","e","h"]
```

**Example 2:**

```
Input: s = ["H","a","n","n","a","h"]
Output: ["h","a","n","n","a","H"]
```

 

**Constraints:**

- `1 <= s.length <= 105`
- `s[i]` is a [printable ascii character](https://en.wikipedia.org/wiki/ASCII#Printable_characters).



#### 🎈 내 풀이

Version1

```
class Solution:
    def reverseString(self, s: List[str]) -> None:
        """
        Do not return anything, modify s in-place instead.
        """
        s[:]=s[::-1]
        
```

s=s[::-1]으로 해도 슬라이싱이 되어야 하는 것이 맞지만 leetcode플랫폼에서는 이를 오류로 처리하기 때문에 s[:]==s[::-1]로 표기해주어야 한다.



Version2

```
class Solution:
    def reverseString(self, s: List[str]) -> None:
        """
        Do not return anything, modify s in-place instead.
        """
        s.reverse()
        
```

가장 기본적인 파이썬에서 리스트를 역순으로 처리하는 방식이다.



Version3

```
class Solution:
    def reverseString(self, s: List[str]) -> None:
        """
        Do not return anything, modify s in-place instead.
        """
        left, right=0, len(s)-1
        while left<right:
            s[left],s[right]=s[right],s[left]
            left+=1
            right-=1
```

투 포인터를 사용한 방식이다. 2개의 포인터를 이용하여 범위를 조절하여 풀이하게 된다.



#### 출처

https://leetcode.com/problems/reverse-string

