---
layout: schedule
permalink: /ems/2024-25/schedule/
title: Schedule
---
A brief summary of the plan for the lecture, what went on in class and exercises related to what we did and what we will be possibly doing next time.

#### <a id="contents">Contents </a>
- <a href="#day_01">Day 01</a>
  - <a href="#day_01_plan">Plan for the day</a>
  - <a href="#day_01_done"> What we did</a>
  - <a href="#day_01_todo"> What to do next time<a>
- <a href="#day_02">Day 02</a>
  - <a href="#day_02_plan">Plan for the day</a>
  - <a href="#day_02_done"> What we did</a>
  - <a href="#day_02_todo"> What to do next time<a>
- <a href="#day_03">Day 03</a>
  - <a href="#day_03_plan">Plan for the day</a>
  - <a href="#day_03_done"> What we did</a>
  - <a href="#day_03_todo"> What to do next time<a>
{% assign current_module = 0 %}
{% assign skip_classes = 0 %}
{% assign prev_date = 0 %}

{% for item in site.data.ems_2024_25_schedule %}
{% if item.date %}
{% assign lecture = item %}
{% assign event_type = "upcoming" %}
{% assign today_date = "now" | date: "%s" | divided_by: 86400 %}
{% assign lecture_date = lecture.date | date: "%s" | divided_by: 86400 %}
{% if today_date > lecture_date %}
    {% assign event_type = "past" %}
{% elsif today_date <= lecture_date and today_date > prev_date %}
    {% assign event_type = "warning" %}
{% endif %}
{% assign prev_date = lecture_date %}

<tr class="{{ event_type }}">
    <th scope="row">{{ lecture.date }}</th>
    <td>
        {{ lecture.plan-title }} <br/>
        <ul>
            {% for topic in lecture.plan-topics %}
            <li style="font-size:12px;">{{ topic }}</li>
            {% endfor %}
        </ul>
        {{ lecture.done-title }} <br/>
        <ul>
            {% for topic in lecture.done-topics %}
            <li style="font-size:12px;">{{ topic }}</li>
            {% endfor %}
        </ul>
        {{ lecture.todo-title }} <br/>
        <ul>
            {% for topic in lecture.todo-topics %}
            <li style="font-size:12px;">{{ topic }}</li>
            {% endfor %}
        </ul>
    </td>
    <td>
        <ul>
            {% for reading in lecture.readings %}
            <li style="font-size:12px;">{{ reading }}</li>
            {% endfor %}
        </ul>
    </td>
</tr>
{% else %}
{% assign current_module = current_module | plus: 1 %}
{% assign module = item %}
<tr class="info">
    <td colspan="5" align="center"><strong>{{ module.title }}</strong></td>
</tr>
{% endif %}
{% endfor %}
