---
layout: post
title: django template extending
---

장고는 웹사이트 내 서로 다른 페이지에서 html을 재사용할 수 있는 템플릿 확장 기능을 제공한다. 웹의 상단인 nav bar나 하단의 footer를 모든 html 파일에 넣지 않고,  base.html 같이 공통으로 사용할 기본 템플릿이 될 html 파일에 넣어 확장해 사용하면 된다.

 

1. 모든 페이지에서 확장해 사용할 공통 html파일인 base.html을 생성하고 아래와 같이 작성한다.

단, css와 같은 static 파일을 사용하기 위해 맨 상단에 {% load static %}을 붙여준다.

{% load static %}

<html>

<head>

<title>My blog</title>

<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.0.0-beta2/dist/css/bootstrap.min.css" rel="stylesheet" integrity="sha384-BmbxuPwQa2lc/FVzBcNJ7UAyJxM6wuqIj61tLrc4wSX0szH/Ev+nYRRuWlolflfl" crossorigin="anonymous">

<link href='//fonts.googleapis.com/css?family=Lobster&subset=latin,latin-ext' rel='stylesheet' type='text/css'>

<link rel="stylesheet" href="{% static 'css/blog.css' %}">

</head>

<body>

<div class="page-header">

<h1><a href="/">My Blog</a></h1>

</div>

<div class="content container">

<div class="row">

<div class="col-md-8">

{% block content %}

{% endblock %}

</div>

</div>

</div>

</body>

</html>

 

 

2. 다른 html 페이지에서 base.html 을 확장해 사용한다.

{% extends 'base.html' %}

{% block content %}

{% for post in posts %}

<div class="post">

<div class="date">

{{ post.published_date }}

</div>

<h1><a href="">{{ post.title }}</a></h1>

<p>{{ post.text|linebreaksbr }}</p>

</div>

{% endfor %}

{% endblock %}
