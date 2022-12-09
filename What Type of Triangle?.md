### What Type of Triangle?
###### Create a function which returns the type of triangle, given the side lengths. Return the following values if they match the criteria.
- No sides equal: "scalene"
- Two sides equal: "isosceles"
- All sides equal: "equilateral"
- Less or more than 3 sides given: "not a triangle"

### Examples
```
get_triangle_type([2, 6, 5]) ➞ "scalene"

get_triangle_type([4, 4, 7]) ➞ "isosceles"

get_triangle_type([8, 8, 8]) ➞ "equilateral"

get_triangle_type([3, 5, 5, 2]) ➞ "not a triangle"
```

### Code
```ruby
def get_triangle_type(arr)
	
end

get_triangle_type([2, 6, 5]) # "scalene"
get_triangle_type([4, 4, 7]) # "isosceles"
get_triangle_type([8, 8, 8]) # "equilateral"
get_triangle_type([3, 5, 5, 2]) # "not a triangle"
```

### Solution
```ruby
def get_triangle_type(arr)
  arr.length != 3 ? "not a triangle" : 	["equilateral", "isosceles", "scalene"][arr.uniq.size-1]
end

def get_triangle_type(arr)
  return "not a triangle" if arr.length != 3
  case arr.uniq.length
    when 3
      "scalene"
    when 2
      "isosceles"
    when 1
      "equilateral"
  end
end

def get_triangle_type(arr)
  return 'scalene' if arr.count == 3 && arr.uniq.count == 3
  return 'isosceles' if arr.count == 3 && arr.uniq.count == 2
  return 'equilateral' if arr.count == 3 && arr.uniq.count == 1
  'not a triangle'
end
```
