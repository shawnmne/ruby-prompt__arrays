---
title: Arrays
instructor_notes: Feel free to re-organize the headings (or add/remove headings) below. We included the headings for your benefit, but it's 100% fine if you want to write your responses in some different structure.
---

# What is an Array?

Arrays are ordered, integer-indexed collections of any objects.

# What are some examples of information that would be Arrays as opposed to some other data type?

groups of information
colors = Array["red", "blue", "yellow", "orange", "green", "purple", "grey", "black", "white"]
testscores = Array[100,88,97,76,92]

# What is one way, using Ruby, to retrieve the 6th element in an Array? How about the 8th element? What happens if you try to retrieve the value of the _9999th_ element (or some element that doesn't exist in the array)?
puts "#{colors[5]}" to access the 6th element
puts "#{colors[7]}" to access the 8th element
returns nil for elements out of range

# The previous question asks about finding, for example, the 6th element in an Array. Is it possible to find the **-6th** (Notice the negative symbol!) element in an Array? What does that even mean?

A negative index is assumed relative to the end of the array --- that is, an index of -1 indicates the last element of the array, -2 is the next to last element in the array, and so on
put "#{colors[-6]}" would output orange

# How would you perform an operation on every element inside an Array?

use .map to perform operations on all elements  
to increase every testscore by 5
testscores.map { |i| i + 5 }

# How do you add elements to an Array?

to add element use .push, .unshift, .insert. <<
colors.unshift("bronze")
colors.push("silver")
colors.insert(4, "gold")
colors << "platinum"

# Given the Array `["Laura", "Fiona", "Tori"]`, how would you replace `"Fiona"` with `"Florence"` so that you end up with `["Laura", "Florence", "Tori"]`?

to replace Fiona use Index of 1 assign it the value of "florence" or if in an unknow array use .index to determine to it's index.  If the item is not in the array you would get a nil and hopefully the code around it would be setup 
for error catching.

names = Array["Laura", "Fiona", "Tori"]
names[1] = "Florence"
names[names.index("Fiona")] = "Florence"

# What do the methods `push`, `pop`, `shift`, and `unshift` do?

'push' is used to add the specified element value to the end of an array.
'pop' deletes the final element from an array and returns it
'shift' returns the first element of an array, deletes that element, and shifts all the other elements down one location to fill the empty spot.
'unshift' shifts all elements of an array up one and add the specified element value to the front of the array

# How do you determine how many elements are in an Array?

To determine how many elements in an array use either .size or .length

# How would you reverse the order of elements in an Array?

use .reverse!

testscores.reverse!
puts "#{testscores}"n   

outputs {92, 76, 97, 88, 100]

# How would you convert a String `"Sumeet Jain"` into an Array `["Sumeet", "Jain"]`? How about to `["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]`? How would you convert the Array back into a String?

name = "Sumeet Jain".split(/ /) would create an array called name with elements ["Sumeet", "Jain"]

use .join method on the array to create a string
apart = Array["S", "u", "m", "e", "e", "t", " ", "J", "a", "i", "n"]
together = apart.join