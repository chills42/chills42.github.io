---
layout: post
title:  "Idiomatic Style"
date:   2015-10-22
categories: programming
---

I've been thinking a lot lately about the reasons I care so much about
programming style. On one hand, it takes a lot of time to worry about getting
it right, and sometimes I feel like I'm overly nit-picky in code reviews.
However, on the other hand, there really is a lot of value in the
extra effort.

Especially as a new programmer, I remember feeling the need to follow the
style guide of a project out of an obedience to the rules. Simply because
a rule existed, I needed to follow it, and I needed to correct code that
failed to follow the rules.

For example:

{% highlight C# %}
public class helloWorld
{
  public helloWorld() { num = 10; }
  public Int32 num {get;set;}
}
{% endhighlight %}

Would fail many of the common guidelines for C# and would need to be 'fixed'.

{% highlight C# %}
public class HelloWorld
{
    public int Number { get; set; }

    public HelloWorld()
    {
        Number = 10;
    }
}
{% endhighlight %}

Ahh... much better. But really, while this fits common style guides better,
what have we actually gained?

Initially, not that much. The interface is marginally nicer since it now fits
the common expectations. Beyond that, it is functionally identical, and
anything already using it would need to be changed since it broke the
interface.

As with most decisions, there are arguments for both. Looking back though, I
realize that strict adherance to style guidelines should not be the goal.
Idiomatic code should be the goal instead. While a style guide will help to
lead you in the right direction, it will not necessarily take you all the way.

A ruby example this time:

{% highlight ruby %}

def AllTheFirstLetters(myList)
    letters = ''
    myList.each do |word|
      letters << word[0]
    end
    return letters
end

{% endhighlight %}

This is an example of code you might see from someone new to ruby. It would
work decently well but is not typical of the code you would normally see. By
applying typical style-guide rules it starts looking a lot more like what a
rubyist would expect.

{% highlight ruby %}

def all_the_first_letters(my_list)
  letters = ''
  my_list.each do |word|
    letters << word[0]
  end
  letters
end

{% endhighlight %}

However, the remaining code is still not truly idiomatic. An expert rubyist
would write something that is a little clearer and makes better use of the
language features.

{% highlight ruby %}

def all_the_first_letters(my_list)
  my_list.each_with_object('') { |word, letters| letters << word[0] }
end

{% endhighlight %}

This may be unfamiliar to someone new to the language, but to someone with
experience, this is not only clear, but expected. Additionally, this is what we
want to strive for, because when you make use of the most common language
idioms, the code is easiest to read later, and the areas that are not idiomatic
become more visible.

That visibility points out code that may need greater attention during later
maintenance or changes, because it tends to be code that provides integration
with other systems, was copied in from somewhere else, or was written by
someone new to the language.

