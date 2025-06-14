---
layout: essay
type: essay
title: "Good or Bad: Question Edition"
# All dates must be YYYY-MM-DD format!
date: 2025-06-13
published: true
labels:
  - Questions
  - Answers
  - StackOverflow
---

<img width="300px" class="rounded float-start pe-4" src="../img/smart-questions/rtfm.png">

## What makes a question "good"?

I'm sure we all have our own conception of what a "good" question looks like. In the essay "How To Ask Questions The Smart Way" by Eric Steven Raymond, the author provides a basic framework or guideline that people with not only professional careers but anyone in general can follow to ensure that they're maximizing learning by asking questions correctly. 

1. Specific - good questions are specific and precise. Explain exactly what it is that you want to know and what ways you can solve the issue at hand.
2. Implementation - good questions include the trial and error process that the individual took that led them to where they are.
3. Curiousity- good questions are also curious in nature. After getting stumped by a problem, take the time to figure out ways you can solve the problem before asking a question. This ensures that questions are asked in a way that seeks understanding and not just answers.

Good questions aren't just singular sentences how generic questions might be, but more of a dialogue that seeks to understand. Once questions are answered and solutions are reached, those same questions can then be turned into learning experiences for other people who may have similar questions in the future. 

## What makes a question "bad"?

We also have a conception of what "bad" questions look like. "Bad" questions are often times a lot easier to recognize than "good" questions. Sometimes people can categorize questions as "bad" just simply based on the fact that they don't like the question. So let's take a look at what can make a question "bad".

1. Generic/Vague - bad questions are almost always generic or vague in nature. Questions asked in this manner make it hard for other individuals to understand what it is that's wrong or what they can even do to help. One sentence questions also fall victim to being generic or vague.
2. Lack of understanding - bad questions also tend to lack the understanding of whatever it is that you're working on. It is this lack of understanding that causes questions to become generic or vague. It shows that the individual didn't take the time to understand the material or work through solutions on their own.
3. Answer hunting - bad questions almost always just ask what the solution is. This shows that the individual is looking for answers as opposed to an understanding of the issues presented before them.

"Bad" questions can often times present the asker in a negative way. So ditch the "bad" questions and start asking some good ones!

```
Q: python date of the previous month

I am trying to get the date of the previous month with python. Here is what i've tried:

str( time.strftime('%Y') ) + str( int(time.strftime('%m'))-1 )

However, this way is bad for 2 reasons: First it returns 20122 for the February of 2012 (instead of 201202) 
and secondly it will return 0 instead of 12 on January.

I have solved this trouble in bash with:

echo $(date -d"3 month ago" "+%G%m%d")

I think that if bash has a built-in way for this purpose, then python, much more equipped, should provide something 
better than forcing writing one's own script to achieve this goal. Of course i could do something like:

if int(time.strftime('%m')) == 1:
    return '12'
else:
    if int(time.strftime('%m')) < 10:
        return '0'+str(time.strftime('%m')-1)
    else:
        return str(time.strftime('%m') -1)
        
I have not tested this code and i don't want to use it anyway (unless I can't find any other way:/)

Thanks for your help!
```

While the heading of his question could be better, it does convey what he’s trying to figure out. Usually something as brief as “python date of previous month” is what other users would enter in as search terms on Google, making it easily found. Another good thing about the question is that it’s not just a question. The asker shows what he or she has done and that he or she has put in some effort to answer the question. And while it may not be as important as the question itself, the asker shows courtesy, which does increase the chance of getting an answer.

```
A: datetime and the datetime.timedelta classes are your friend.

1. find today
2. use that to find the first day of this month.
3. use timedelta to backup a single day, to the last day of the previous month.
4. print the YYYYMM string you're looking for.

Like this:

 >>> import datetime
 >>> today = datetime.date.today()
 >>> first = datetime.date(day=1, month=today.month, year=today.year)
 >>> lastMonth = first - datetime.timedelta(days=1)
 >>> print lastMonth.strftime("%Y%m")
 201202
 >>>

```
 
The asker received six possible answers, and he or she was successful in inciting discussion from multiple users. The answers themselves were clear and were devoid of the rumored sarcasm and hostility of “hackers.” Since I myself have referenced this page and found it useful, I can confidently say that it is a good question.

## The foolproof way to get ignored.

While there are decent questions that benefit everyone, there are those one can ask to create an entirely different effect. In the following example, a user asks how he would, in short, create a desktop application with Facebook.

```
Q: Facebook Desktop Notifier

I am a beginner programmer that have never used anything other than what's included in a language.

I am trying to create a desktop application that notifies me anytime I get an update onfacebook. 
How should go about doing this? Thanks in advance.

edit Sorry I was not clear. Is there any way to make a DESKTOP application with facebook?
```

A simple “yes” would have answered the question, but we know that’s not the sort of answer he or she is looking for. Fortunately, someone kindly responded with a link to Facebook’s developer website. The asker should have done more research on his or her potential project. Then further down the road, he or she could have asked more specific and detailed questions that wouldn’t require a thousand-paged response for a sufficient answer.

## Conclusion

When we rely on others’ generosity and expertise to provide answers to our questions, it should hold that the question we ask should be one that leads to efficient and effective help that not only benefits us, but also the people we ask and others who might ask the same question in the future. Thus, if you have a question… make it a smart one! Asking questions may not always get you the best answer, but asking them in a way that will make others want to answer them will increase the success of finding a good solution and make it a positive experience on all sides.
