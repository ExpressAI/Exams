# Exam

College Entrance Examination Data from 2017 - 2021

| Year | Type           | Sources                                                                                                                                                                             | Finished |
|------|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------|
| 2017 | 2017全国卷I       | 1. https://wenku.baidu.com/view/9587128051e2524de518964bcf84b9d528ea2ca5.html?re=view                                                                                               | [ ]      |
| 2017 | 2017全国卷II      | 1. https://wenku.baidu.com/view/a7a47751ef06eff9aef8941ea76e58fafab04599.html?re=view                                                                                               | [ ]      |
| 2017 | 2017全国卷III     | 1. http://m.2abc8.com/wap-action-69878-1.htm                                                                                                                                        | [ ]      |
| 2018 | 2018新课标全国卷I卷   | 1. https://wendang.xuehi.cn/doc/0571c585ba4cf7ec4afe04a1b0717fd5360cb2d5.html                                                                                                       | [ ]      |
| 2018 | 2018新课标全国卷II卷  | 1. https://wenku.baidu.com/view/0b327ba029ea81c758f5f61fb7360b4c2f3f2a7d.html?re=view                                                                                               | [ ]      |
| 2018 | 2018新课标全国卷III卷 | 1. https://wenku.baidu.com/view/ee57b52a24c52cc58bd63186bceb19e8b8f6ec3c.html?re=view                                                                                               | [ ]      |
| 2019 | 2019全国卷I       | 1.http://www.liaoweiwei.com/2019gaokao-word.html                                                                                                                                    | [ ]      |
| 2019 | 2019全国卷II      | 1.http://www.liaoweiwei.com/2019gaokao-word.html                                                                                                                                    | [ ]      |
| 2019 | 2019全国卷III     | 1.http://www.liaoweiwei.com/2019gaokao-word.html                                                                                                                                    | [ ]      |
| 2020 | 2020全国卷I       | 1.https://www.gk100.com/read_7708.htm <br/>2.https://zhuanlan.zhihu.com/p/160136755                                                                                                 | [ ]      |
| 2020 | 2020全国卷II      | 1. https://www.gk100.com/read_7709.htm                                                                                                                                              | [ ]      |
| 2020 | 2020全国卷III     | 1. https://www.gk100.com/read_7711.htm                                                                                                                                              | [ ]      |
| 2020 | 2020全国新高考I卷    | 1. https://www.sohu.com/a/435305611_578753                                                                                                                                          | [ ]      |
| 2020 | 2020全国新高考II卷   | 1. http://www.yygrammar.com/Article/202012/5533.html                                                                                                                                | [ ]      |
| 2021 | 2021全国甲卷       | 1. https://www.gaokzx.com/Fup/document/202108/08-16_181733-10105.pdf                                                                                                                | [ ]      |
| 2021 | 2021全国乙卷       | 1. https://edu.sina.com.cn/gaokao/2021-06-08/doc-ikqciyzi8491406.shtml                                                                                                              | [ ]      |
| 2021 | 2021新高考I卷      | 1.[https://www.bilibili.com/read/cv11699209](https://www.bilibili.com/read/cv11699209)<br/>2.[https://www.cpsenglish.com/question/50938](https://www.cpsenglish.com/question/50938) | [x]      |
| 2021 | 2021新高考II卷     | 1. https://www.doc88.com/p-14361796844805.html                                                                                                                                      | [ ]      |


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

标注注意事项：
1. 一般网上复制过来的东西，有的单词之间可能没有断开，得手动分一下。
2. 单引号双引号可能不是英文的引号，得手动换一下。
3. 注意去掉阅读或者其他题目中可能出现的中文。（中文仅能出现在name，description，或者翻译题目中）
4. 听力原稿一般与题目分开，可以单独寻找资源

NOTES:
1. 全国卷的听力有很多是重复的

## Essays
作文题目可以有以下来源：
1. [https://news.koolearn.com/20170527/1121593.html](https://news.koolearn.com/20170527/1121593.html) 中的2006年～2012年
2. [https://www.gaokzx.com/c/202104/51072.html](https://www.gaokzx.com/c/202104/51072.html) 
3. [https://www.gk100.com/read_14808.htm](https://www.gk100.com/read_14808.htm)

对于作文题一般有以下几种形式供参考：
1. pure-writing
如果没给开头/结尾：
```
{
  "source": "2016高考英语满分作文范文(新课标1卷)", 
  "link": "http://gaokao.koolearn.com/20170527/1104693.html", 
  "question_type": "pure-writing", 
  "question": "假定你是李华，暑假想去一家外贸公司兼职，已写好申请书和个人简历(resume)。给外教Mr Jenkins 写信，请她帮你修改所附材料的文字和格式(format)", 
  "requirements": "1. 词数100左右; 2. 可以适当增加细节，已使行文连贯。", 
  "example_essay": "Dear Ms Jenkins, I am Li Hua, I am writing to tell you something about my plan for the coming summer vacation and I also want you to do me a favor. In order to get some practical experience, I am planning to take a part-time job in a foreign capital company. I have already finished my job application and personal resume. But this is the first time that I have written an application and the personals resume, so I don't even know if there are something to pay attention to. So, I'm writing you the letter , hoping you can give me some help. I will be very grateful if you can help me. Looking forward to your reply. And I'd be really thankful. Yours, Li Hua"
}
```
如果给了开头/结尾, （若只给开头，则只写start这一项）
```
{
  "source": "高考英语作文：2014高考英语满分作文(安徽卷)", 
  "link": "https://gaokao.koolearn.com/20150424/853875.html", 
  "question_type": "pure-writing", 
  "question": "为了帮助中学生健康成长，某中学英文报开辟了“HEART-TO-HEART”专栏。假设你是该栏目的编辑Jamie，收到一封署名为Worried的求助信。信中该同学向你诉说了自己的困扰：近日容易发脾气，使正常的学习和生活受到了影响。请用英文给该同学写一封回信。内容要点如下：1.表示理解并给予安慰;2.提出建议并说明理由。", 
  "requirements": "1.词数120左右; 2.信中不能出现与本人相关的信息; 3.信的开头与结尾已为你拟好，不计入总词数。", 
  "start": "Hi Worried， I’m sorry to know that you’re having such a had time at the moment.", 
  "end": "Yours, Jamie", 
  "example_essay": "Hi Worried, I'm sorry to know that you're having such a bad time at the moment. The truth is that everyone will have one of those periods when things seem to be going wrong, so you don't have to worry much. The important thing is to learn to control your temper so that you may not do or say anything you’ll regret. Here are three useful tips: First, talk to someone you trust about how you feel. This is a good way of letting your anger out without hurting others or yourself. Second, go outdoors and play team games with your ftiends as physical exercise is an effective way to get rid of anger. And third, remain optimistic about your future. Such a positive attitude towards life can be helpful in lifting your spirits. I hope you'll soon feel calmer and carry on as normal. Yours, Jamie"}
```
2. reading-writing
```
{
  "source": "2016高考英语满分作文范文(江苏卷)", 
  "link": "https://gaokao.koolearn.com/20170527/1104698.html", 
  "question_type": "reading-writing", 
  "reading": "In recent years, internet voting has become increasingly popular in China. People not only cast on-line votes themselves, but also urge others to vote for competitions like the \"Most Beautiful Teacher\" and the \"Cutest Baby\". Li Jiang, a high school student, is invited to vote in the \"Best Police Officer\" competition, organized by the local government to let the public have a better understanding of police officers' daily work. Li Jiang visits the website and reads all the stories. He is deeply moved by their glorious deeds. He is already thinking of becoming a policeman himself in the future. Su Hua is invited by his uncle to vote for his cousin in the \"Future Singer\" competition. He has already received three similar invitations this week. His uncle tells him that if his cousin wins the competition, the family will win an oversea s tour for free. Su Hua likes his cousin very much, but he finds other singers perform even better. To vote, or not to vote This is a question that troubles him very much.", 
  "question": "1. 用约30个单词写出上文概要; 2. 用约120个单词阐述你对网络投票的看法，并用2 ~3个理由或论据支撑你的看法。", 
  "requirements": "1. 写作过程中不能直接引用原文语句; 2. 作文中不能出现真实姓名和学校名称; 3. 不必写标题。",
  "example_essay": "On-line voting becomes increasingly popular, and many competitions get people involved in it. It is beneficial to some people, while it puts others into a dilemma over whether to vote or not. In my opinion, on-line voting is an inseparable part of modern life and should be welcomed, since it is no more than a way to participate in public life. It makes no difference from ordinary voting events, in which candidates go around to seek supports. In addition, the Internet makes surveying and voting easy and convenient, regardless of time and space. Furthermore, voting on the Internet makes instant feedback possible. To be honest, voters sometimes feel annoyed, not because they hate voting, but because they are divided between emotion and fairness. Things will turn for the better if we can work out some participation rules for people to obey. Therefore, I hold a positive attitude towards on-line voting."
}
```

注意事项
1. 所有的范文中的单引号双引号句号等都需转换成英文的单引号双引号句号等
2. "注意"中的内容可以放在requirements里。如果没有明确requirements，则不需要写requirements这一项。
3. 圆圈数字列点的等等都转化成1. 2. 3.这种
4. 涉及到图片的题目可以忽略不整理
5. 无需列出参考词汇
6. 对于每篇好作文都整理成上述形式，一个题目的多篇作文就可以写多个上述结构，一个占一行。
7. 范文中的中文要去掉。
