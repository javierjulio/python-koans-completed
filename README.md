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
* When `range()` has 1 argument thats the *stop* value. With 2: start and stop. With 3: start, stop and step

  ```python
  list(range(3))    # [0, 1, 2]
  list(range(3, 6)) # [3, 4, 5]
  ```

* Using `insert()` will place element before the one at given index

  ```python
  nums = [1, 2, 3]
  nums.insert(123, 1) # [1, 123, 2, 3]
  ```

* The Dictionary `fromkeys()` method takes a sequence argument and then second argument is a default value for each key. There are 3 basic sequence types: lists, tuples, and ranges. *Tuples* are defined with *parentheses*. For example:

  ```python
  letters = {}.fromkeys(('A', 'B', 'C'), 23)
  letters['A'] # 23
  letters['B'] # 23
  ```

* Tuples are *immutable* so item assignment isn't possible unless for example you convert to a list, add/remove values and make into a tuple again. *Tuples are less flexible than lists, but faster*.
* Creating a `tuple` or `set` using constructor can be surprising.

  ```python
  ('Surprise!')       # ('Surprise!')
  tuple('Surprise!')  # ('S', 'u', 'r', 'p', 'r', 'i', 's', 'e', '!')
  
  {'12345'}     # {'12345'}
  set('12345')  # {'1', '2', '3', '4', '5'}
  ```

* Unlike Ruby the last line in a method *does not* return that value. Need to use `return` statement. Also methods must be called using parens.

  ```python
  def pointless_method(self, a, b):
    sum = a + b

  self.pointless_method(1, 2) # -> None
  ```

* The `pass` statement acts as a placeholder. For example, if you want to define a method but not have it do anything at the moment you can use `pass` so the code will run otherwise it won't (you'd get an `IndentationError`)

  ```python
  class User(object):
    def first_name(self):
        pass

    def last_name(self):
        print("Last Name")
  ```

* Methods and control statements end in a colon. Methods always must be called using parens.

  ```python
    def empty_method(self):
      pass
    
    if True:
      print("true")
    else:
      print("false")
    
    i = 1
    while i <= 10:
      print(i)
      i += 1
    
    countries = ['Argentina', 'Spain', 'Italy']
    for country in countries:
      print(country)
    
    names = [('Lionel', 'Messi'), ('David', 'Villa')]
    for first_name, last_name in names:
      print(first_name, last_name)
  ```

* Dictionaries are key-value pairs while Sets are unordered collections with no duplicate elements.
* ...
