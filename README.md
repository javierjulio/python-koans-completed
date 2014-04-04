# python-koans-completed

This is my attempt at completing all the tests in Python Koans using Python 3. Since I'm learning Python along the way I have included 
in depth notes as I complete each of the test files for reference.

## Notes

* Booleans are capitalized: `True` and `False`
* Method name ends in a colon and no ending indicator (whitespace sensitive like CoffeeScript?)
* Like `nil` in Ruby, `None` in Python is an object and `None` is *falsy*
* Since Koans use `is` and `is not` the difference ([source](http://stackoverflow.com/a/4485254/941579)):
  * `==` and `!=` test if objects have the same value
  * `is` and `is not` test if objects are the same object (same as checking object ids)
  * Seems like Ruby, its advised to avoid `is` and `is not`
* When `range()` has 1 argument thats the *stop* value, but with 2 its start and stop
  ```python
  list(range(3))    # [0, 1, 2]
  list(range(3, 6)) # [3, 4, 5]
  ```
* Using `insert()` will place element before the one at given index
  ```python
  nums = [1, 2, 3]
  nums.insert(123, 1) # [1, 123, 2, 3]
  ```
* ...
