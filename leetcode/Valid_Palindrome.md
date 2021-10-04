### ✨문제
Given a string `s`, determine if it is a palindrome, considering only alphanumeric characters and ignoring cases.

**Example 1:**

```
Input: s = "A man, a plan, a canal: Panama"
Output: true
Explanation: "amanaplanacanalpanama" is a palindrome.
```

**Example 2:**

```
Input: s = "race a car"
Output: false
Explanation: "raceacar" is not a palindrome.
```

**Constraints:**

- `1 <= s.length <= 2 * 105`
- `s` consists only of printable ASCII characters.

#### 🎈 내 풀이

```
class Solution:
    def isPalindrome(self, s: str) -> bool:
        s = s.lower()
        s = re.sub('[^a-z0-9]','',s)
        return s==s[::-1]
```

슬라이싱과 정규식을 이용한 풀이이다.
슬라이싱은 내부적으로 C로 구현되어있기 때문에 빠른 속도를 구사한다.

#### 출처
https://leetcode.com/problems/valid-palindrome/
