---
layout: questions
title: "Some intro questions..."
button: next page
pageNo: 1
---
Questions are written down in a format similar to markdown, and markdown can be used in the labels:

{% multiple_choice name:"radiobutton" type:"radio" %}
# Question 1

[ ](answerA) A: Option 1
[](answerB) B: Option 2
[X](allAbove) C: All of the above
{% endmultiple_choice %}


{% multiple_choice name:"radiobutton" type:"checkbox" %}
# Question 2
(multiple options are possible)
[ ](option 1) option 1
[X](option 2) option 2
[ ](option 3) option 3
{% endmultiple_choice %}

## Likert scales
A common question type is the Likert scale. This question-type is easy to create this as well:

{% likert name:"emotion" %}
# Question 3
[ ](str_agree) strongly agree
[](agree) agree
[](neutral) neutral
[](disagree) disagree
[](str_disagree) strongly disagree
{% endlikert %}

## Free text
There are two types of free text possible, a text-area and a text-box.

Question 4.


{% text_input name:"clarification" type:"textarea" %}
# How would you improve the javascript above?
_you can write an example below_
[Thoughts and clarification](clarification)
{% endtext_input %}

## Combined questions
It's also possible to group inputs in one question-block (as long as they are the same type):

{% text_input name:"contact" %}
# What's your name?
[First and last name](name) Your full name _optional_

# What's your email-address?
[something@server.com](email) _optional_
{% endtext_input %}

## Storing answers
Answers can be stored in any backend of your choosing, by default Firebase. Answers are stored when participants click next page.

## Pairwise comparison
The next page demonstrates pair-wise comparison.
