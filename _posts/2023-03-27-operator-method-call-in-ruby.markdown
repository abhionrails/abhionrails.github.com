---
layout: post
title: Operator method call in Ruby
categories: Ruby
tags: Operator method call in Ruby
description: Operator method call in Ruby
---
In Ruby, you can call methods on objects using the dot notation. However, there is an alternative way to call methods on objects, which is called the operator method call. In this blog post, we will explore what operator method call is, how it works, and when you might want to use it.

What is operator method call?

In Ruby, many operators such as "+", "-", "*", and "/" are actually method calls on objects. For example, when you add two numbers with the + operator, you are actually calling the "+" method on the left-hand side operand, passing the right-hand side operand as an argument.
Operator method call is a way to call methods using the operator syntax, instead of the dot notation. For example, instead of writing "a + b", you can write "a.+(b)".

How does it work?

To use operator method call, you need to define the corresponding method for the operator. For example, if you want to use the "+" operator to add two objects of your custom class, you need to define the "+" method for that class.

Here's an example:

```ruby
class MyClas
  attr_accessor :value

  def initialize(value)
    @value = value
  end

  def +(other)
    MyClass.new(@value + other.value)
  end
end

a = MyClass.new(10)
b = MyClass.new(20)
c = a + b # calls the "+" method on a, passing b as an argument
puts c.value # prints 30
```

In this example, we define a custom class MyClass with a "+" method that adds the values of two MyClass objects and returns a new MyClass object with the result.

When we create two MyClass objects "a" and "b" with values 10 and 20, respectively, we can use the "+" operator to add them together. This calls the "+" method on "a" with "b" as an argument, creating a new MyClass object "c" with the value of 30.

When should you use operator method call?

Operator method call is not used very often in Ruby, as the dot notation is the more common way to call methods. However, there are a few cases where operator method call can be useful.

One example is when defining mathematical operations on custom classes, as we saw in the previous example. Another example is when defining comparison operators such as "<" and ">". For example:

```ruby
class MyClas
  attr_accessor :value

  def initialize(value)
    @value = value
  end

  def <(other)
    @value < other.value
  end
end

a = MyClass.new(10)
b = MyClass.new(20)
puts a < b # calls the "<" method on a, passing b as an argument
```
In this example, we define a custom "<" method for MyClass that compares the value of two MyClass objects. We can then use the "<" operator to compare two objects of MyClass.

Conclusion

Operator method call is a way to call methods on objects using the operator syntax, instead of the dot notation. It is not used very often in Ruby, but can be useful when defining mathematical or comparison operations on custom classes.