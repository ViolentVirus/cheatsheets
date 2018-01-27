# Ruby Cheat-sheet

## Strings
```ruby
string[index]               # single char
string[start, length]       # 
string[range]               # e.g., 1..4, -1 for last char
```
## Arrays
```ruby
my_array = Array.new # or []    # Empty array
my_array << "first!"            # append to array
```

### Methode
```ruby
Array.count(ele)
Array.find_all { |ele| # boolean expression }
```
### Slicing Arrays
```ruby
array[index]                # single look-up
array[start, length]        # subset (inclusive)
array[range]                # subset 1..5 (inclusive) or 1...5(exclusive)
array.slice(index)          
array.slice(start, length)  
array.slice(range)          
```
Note: `Array.slice!` alters the original array.
```ruby
Array.shuffle
Array.pop(n)            # pop of last n elements
Array.shift(n)          # pop from beginning
Array.delete_at(i)
Array.delete(element)
```
Array Operators
```ruby
a - b       # Remove commonality
a & b       # Intersect (elements found in both)
a | b       # union (every unique element)
```

### Functional Programming
```ruby
.all? { |ele| #boolean }                # Returns t/f if all satisfy block condition
.inject(0) { |sum, n| sum += n }
.each { |element| #do something }
.select { |n| n > 4 }                   # Like filter
```

## String Methods
```ruby
.capitalize
.upcase
.downcase
.split(str/regex)
.sub("first", "with")
.gsub("orig", "replacement")        # 'global' replace
```

## Scope
Constant lookup operator `::`
```ruby
Module::(method/variable)
Library::Module::(method/variable)
::(method/variable)   # top-most scope
```

## File Opening
```ruby
mode = "r+"     # read/(insert)write
file = File.open("file-name.txt", mode)
file.close
```
`File#open` auto-closes when supplied with a block
```ruby
what_am_i = File.open("clean-slate.txt", "w") do |file|
  file.puts "Call me Ishmael."
end
p what_am_i     # prints nil
```
Modes
```ruby
r   # read
r+  # read/(insert) write
w   # removes existing text
```

## Math
```ruby
float.ceil
float.floor
```

## Lambda
```ruby
my_lamb = { puts "baaahh" }
my_lamb.call
```

## Other stuff
```ruby
rand(n)         # Integers 0 ... (excluding) n
```