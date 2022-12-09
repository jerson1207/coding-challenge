### Hitting the Jackpot
###### Create a function that takes an array (slot machine outcome) and returns true if all elements in the array are identical, and false otherwise. The array will contain 4 elements.
### Examples
```
test_jackpot(["@", "@", "@", "@"]) ➞ true

test_jackpot(["abc", "abc", "abc", "abc"]) ➞ true

test_jackpot(["SS", "SS", "SS", "SS"]) ➞ true

test_jackpot(["&&", "&", "&&&", "&&&&"]) ➞ false

test_jackpot(["SS", "SS", "SS", "Ss"]) ➞ false
```
### Code
```ruby
def test_jackpot(result)

end

p test_jackpot(["@", "@", "@", "@"]) # true
p test_jackpot(["abc", "abc", "abc", "abc"]) # true
p test_jackpot(["SS", "SS", "SS", "SS"]) # true
p test_jackpot(["&&", "&", "&&&", "&&&&"]) # false
p test_jackpot(["SS", "SS", "SS", "Ss"]) # false
```
### Solution
```ruby
def test_jackpot(result)
  result.uniq.count == 1
end

def test_jackpot(result)
  result.all?{ |word| word == result[0]}
end
```
