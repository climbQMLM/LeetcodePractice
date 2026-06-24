# md 模板

两种情况共用题目头部，正文不同。生成时去掉本文件里的说明性括注。

---

## 情况 A 模板（用户能独立完成部分思路 → 按顺序列出所有踩过的思维误区）

```markdown
# 1. Two Sum

- **难度**: Easy
- **链接**: https://leetcode.com/problems/two-sum/

## 知识点 Q&A

（仅当讨论中出现过语法/基础概念类提问时才加这部分，没有就整段省略）

**Q: （用户问的知识点/语法问题，原样或稍微精简地保留问题本意）**

A: （对应的解答，简洁整理）

## 思维误区复盘（按踩坑顺序）

### 1. （第一个误区的简短标题）

**❌ 错误写法**

\`\`\`python
for i in range(n):
    for j in range(n):           # 暴力双循环，O(n^2)
        if nums[i] + nums[j] == target:
            return [i, j]
\`\`\`

**✅ 正确写法**

\`\`\`python
seen = {}
for i, x in enumerate(nums):     # 哈希表，一次遍历 O(n)
    if target - x in seen:
        return [seen[target - x], i]
    seen[x] = i
\`\`\`

### 2. （第二个误区的简短标题，如果有）

**❌ 错误写法**

\`\`\`python
# ...
\`\`\`

**✅ 正确写法**

\`\`\`python
# ...
\`\`\`

（依此类推，把讨论过程中出现过的每一个主要误区都列出来，不要只留最后一个）

## 最终解法

\`\`\`python
def twoSum(nums, target):
    seen = {}
    for i, x in enumerate(nums):
        if target - x in seen:
            return [seen[target - x], i]
        seen[x] = i
\`\`\`

- **时间复杂度**: O(n)
- **空间复杂度**: O(n)
```

---

## 情况 B 模板（用户几乎无法独立完成 → 整段讨论归纳）

```markdown
# 1. Two Sum

- **难度**: Easy
- **链接**: https://leetcode.com/problems/two-sum/

## 知识点 Q&A

（仅当讨论中出现过语法/基础概念类提问时才加这部分，没有就整段省略）

**Q: （用户问的知识点/语法问题）**

A: （对应的解答，简洁整理）

## 思路推导

（把讨论中如何一步步想到解法的过程，重新组织成连贯的讲解。例如：为什么暴力解不够好 → 想到哈希表 → 一次遍历的关键观察。）

## 关键点

- （讨论中点明的关键观察 / 易错点，逐条列出）

## 最终解法

\`\`\`python
def twoSum(nums, target):
    seen = {}
    for i, x in enumerate(nums):
        if target - x in seen:
            return [seen[target - x], i]
        seen[x] = i
\`\`\`

- **时间复杂度**: O(n)
- **空间复杂度**: O(n)
```
