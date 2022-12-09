### Return Only the Integer
###### Write a function that takes an array of elements and returns only the integers.
#### Example
```ruby
return_only_integer([9, 2, "space", "car", "lion", 16]) ➞ [9, 2, 16]

return_only_integer(["hello", 81, "basketball", 123, "fox"]) ➞ [81, 123]

return_only_integer([10, "121", 56, 20, "car", 3, "lion"]) ➞ [10, 56, 20, 3]

return_only_integer(["String",  true,  3.3,  1]) ➞ [1]
```

### Code
```ruby
def return_only_integer(arr)
  
end

p return_only_integer([9, 2, "space", "car", "lion", 16]) # [9, 2, 16]
p return_only_integer(["hello", 81, "basketball", 123, "fox"]) # [81, 123]
p return_only_integer([10, "121", 56, 20, "car", 3, "lion"]) # [10, 56, 20, 3]
p return_only_integer(["String",  true,  3.3,  1]) # [1]
```

### Solutions
```ruby
def return_only_integer(arr)
  arr.grep Integer
end

def return_only_integer(arr)
  arr.select {|elem| elem.is_a?(Integer)}
end

```

https://www.rubyguides.com/2018/10/grep-method-with-examples/

