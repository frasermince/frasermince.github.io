---
layout: post
title:  "Composition Over Inheritance"
date:   2015-06-07 22:53:45
categories: Refactoring Ruby
---
In the world of Object Oriented Programming inheritance is often a standard feature. Because of this many developers do not realize the added complexity that comes with inheritance. In this article I will be discussing why inheritance in Ruby should generally be avoided and alternate approaches that can be taken. We will compare two different pieces of code and see the benefits of both. The dangers of inheritance are not immediately clear 

Instead of inheritance in Ruby we want to use composition. So instead of making classes in Ruby inherit from other classes we want to make objects that include other classes as parameters and instance variables. This allows pieces to be used in isolation from each other. In the next 

Inheritance
{% highlight ruby %}
class Library
  include fileable
end
{% endhighlight %}

class Library
  def initialize
    @
  end
end
