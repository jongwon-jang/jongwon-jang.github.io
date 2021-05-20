---
title: "Swift Journey No.2 - More Data Types"
date: 2021-05-19 22:00:00 -0500
categories: swift ios
---
# Complex Data Types

## Arrays
Arrays are collections of values that are stored as a single value

```swift
let iphone = "iPhone 12 Pro Max"
let macbook = "Macbook Pro 16"
let ipad = "iPad Pro 12.9"

let apple = [iphone, macbook, ipad]
```

You can read values from an array by writing a number inside a bracket
```swift
apple[1]
```
Swift crashes if you read an item that doesn't exist. (for example, `apple[5]` will produce an error)

## Sets
Sets are collections of values just like arrays, but they have 2 differences
1. Items __aren't stored in orders__ (it is stored randomly)
2. All items must be __unique__

```swift
let colors = Set(["red", "green", "blue", "green", "blue"])
```
`colors` set will only include red, green, and blue once.

## Tuples
Tuples allow you to store several values together in a single value.
Sounds like arrays, but the differences are:
1. You can't add or remove items from a tuple (__size fixed__)
2. You __can't change the type of items__ in a tuple
3. You can access items using __numerical positions__ or by __naming__ them (but cannot read numbers or names that don't exist)

```swift
var name = (first: "Jongwon", last: "Jang")
```
You can access items like:
```swift
name.0
name.first
```

## Arrays vs Sets vs Tuples
If you need a __specific__, __fixed__ collection of related values, use a *tuple*
```swift
let address = (streetNo: 777, street: "Lucky Ave", city: "Toronto")
```

If you need a collection of values that should be __unique__ or to be able to check if there is a __specific item in there__, use a *set*
```swift
let books = Set(["Nike Bio", "Jobs Bio", "Marvel Comic", "Software Testing", "Marvel Comic"])
```
Marvel Comic will only be stored once

If you need a collection that can contain __duplicates__, or the __order matters__, use an *array*
```swift
let languages = ["Python", "Swift", "Java", "Java" ]
```

