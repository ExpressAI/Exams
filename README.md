# Exam

College Entrance Examination Data from 2017 - 2021

| Year | Type      | Sources                                                                                                                                                                             | Finished |
|------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| 2017 |           |                                                                                                                                                                                     | [ ]      |
| 2018 |           |                                                                                                                                                                                     | [ ]      |
| 2019 |           | 1.[http://www.liaoweiwei.com/2019gaokao-word.html](http://www.liaoweiwei.com/2019gaokao-word.html)                                                                                  | [ ]      |
| 2020 | 2020全国卷I  | 1.[https://www.gk100.com/read_7708.htm](https://www.gk100.com/read_7708.htm)<br/>2.[https://zhuanlan.zhihu.com/p/160136755](https://zhuanlan.zhihu.com/p/160136755)                 | [ ]      |
| 2021 | 2021新高考I卷 | 1.[https://www.bilibili.com/read/cv11699209](https://www.bilibili.com/read/cv11699209)<br/>2.[https://www.cpsenglish.com/question/50938](https://www.cpsenglish.com/question/50938) | [x]      |


### 2019
* [全国卷](http://www.liaoweiwei.com/2019gaokao-word.html)



# Schema
可以参考2021。目前不同的大题分开了。
一般情况下每个大题都是如下格式
```json
[
  {
    "name": "第一节",
    "description": "第一节（共15小题；每小题 1分，满分15分）...",
    "question_type": "multiple-choice",
    "content": [
      {
        "context": "听力原稿或者文章",
        "questions": [
          {
            "question_id": 1,
            "question": "what did Bob do?",
            "options": [
              "Doctor",
              "Teacher",
              "Driver"
            ],
            "answer": 0
          }
        ]
      }
    ]
  }
]
```
对于其他题型，可以参考以下：
1. 完形填空请参考 `language.json`里面题型为`independent-cloze-choice`的部分。其中每个空都替换成了`<Q1>`, `<Q2>`这样的placeholder。
2. 对于有几个空需要选，但是这几个空共有一些选项这样子的题型，请参考`reading.json`里面题型为`dependent-cloze-choice`的部分。其中每个空都替换成了`<Q1>`, `<Q2>`这样的placeholder。
3. 对于那些有给了一个词的原型，让你在空里填变形的题型，请参考`language.json`里面题型为`independent-cloze-hint`的部分。其中每个空都替换成了`<Q1>`, `<Q2>`这样的placeholder，并且删掉了括号中的hint。
4. 作文请参考`writing.json`
5. 其他题型如果出现了可以再讨论。

注意事项：
1. 一般网上复制过来的东西，有的单词之间可能没有断开，得手动分一下。
2. 单引号双引号可能不是英文的引号，得手动换一下。

  
