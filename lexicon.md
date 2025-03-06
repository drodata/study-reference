# Lexicon
Vocabulary 的子集，记录“孩子学过的”单词。

结构
--------------------------------------------------------------------------
### Schema
Column                              | Type      | Null | Note
------------------------------------|-----------|------|-------
`id`                                | int       | No   | 
`name`                              | string    | Yes  | 同 vocabulary.name 方便搜索
`type`                              | bool      | No   | Lookup `textbook-vocabulary-type`
`source`                            | bool      | yes  | Lookup `lexicon-source`
`level`                             | bool      | Yes  | Lookup `textbook-vocabulary-level`
`chapter_id`                        | int       | Yes  | 'source` 值是 TEXTBOOK 是必填
`clip_id`                           | bool      | Yes  | 
`question_id`                       | bool      | Yes  | 
`vocabulary_id`                     | bool      | Yes  | 
`expression_node_id`                | bool      | Yes  | 

Types (Lookup `textbook-vocabulary-type`):
- 1: word
- 2: expression

Levels (Lookup `textbook-vocabulary-level`):
- 0: Normal
- 1: Bold   
- 2: Expanded

Sources (Lookup `lexicon-source`):
Code                    | Value  | Note
------------------------|--------|------------
DAILY                   |   0    | 日常看到的零散内容
TEXTBOOK                |   1    | 课本
POST                    |   2    | 文章
QUESTION                |   3    | 题目
''
    const TYPE_WORD = 1;
    const TYPE_EXPRESSION = 2;
