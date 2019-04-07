---
layout: post
title: "5 Simple CSS layouts for popular user inferfaces"
author: "Louis Dickinson"
date: 2019-03-16 00:00:00 +0100
tags: 
  - web-development
  - css
  - ui-design
---

From my interactions with developers in the past, CSS has been at the top of the list of annoying aspects of web development.
The main issue is that CSS doesnt contain any structued logic, its a simple set of instructions which tells the browser how
to render your HTML. In this post I'd like to go over some simple CSS layouts which are easy to implement in your websites.

### Layouts for general web development

We're going to make use of the relatively new flexbox, for anyone wanting to learn more about flex, i'd recommend reading
[Mozila's Basic Concepts of Flexbox][concepts-of-flexbox]. Lets focus on the basics for now.

### 1. Login Form

Lets start off with a simple login form. First we need the stucture of the page.

{% highlight html %}
<main>
  <div class="login">
    <div class="title">
      <form>
        <input type="email">
        <input type="password">
        <button type="submit">Login</button>
      </form>
  </div>
</main>
{% endhighlight %}

Now that we have our simple page structure. Lets start by centering the form on the page.

{% highlight scss %}
main {
  width:100%;
  height:100%;
  justify-content:center;
  align-items:center;
  display:flex;

  .login {
    width:320px;
    height:400px;
    background:gray;
    flex:1;
  }

}
{% endhighlight %}

Now that we have our basic structure we can see the login form centered in the page.

[concepts-of-flexbox]: https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Flexible_Box_Layout/Basic_Concepts_of_Flexbox