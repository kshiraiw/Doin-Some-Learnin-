---
title: "Angular Magic"
---
Today I would like to present the magic that is.... **Angular**! Of course everyone knows about the beauty of 2-way data binding but did you know about ng-bind-html or ng-class? I've discovered both recently while working on personal projects and I don't know how I can live without it! 

<center><img src="https://brijbhushan.files.wordpress.com/2015/02/normal.gif"></center>


ng-bind-html allows you to insert safe html scripts into your website. If you want your clients to be able to format their own html and display it safely on your own site with only one line of code.

{% highlight html %}
<div ng-bind-html="myHtmlString"></div>
{% endhighlight %}

{% highlight javascript %}
$scope.myHtmlString = "<p>blah <strong>blah</strong> <em>blah</em></p>"
{% endhighlight %}

This example will look like this:
blah **blah** *blah*

The client can write his text how he wants to and you don't have to worry about injection scripts.

The other cool thing is ng-class. This allows you to add logic to your css. It is pretty awesome. This allows you to have a dynamic layout. For example, if I want to highlight only people that are your friends, you add a css class to only friends.

The documentation tells you to use it as 

{% highlight html %}
  <div ng-class="{'bold': important}"></div>
{% endhighlight %}

This means, the bold class will only apply when important is true. However, the way that I find ng-class very useful is when I use ternary operators. 

{% highlight html %}
<div ng-class="isChecked ? 'blue' : 'red'"></div>
{% endhighlight %}

If isChecked is true, the class blue will be applied to this tag. If isChecked is false, the class red will be applied. 

I feel like both of these abilities allow you to make awesome projects!