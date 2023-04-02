# Welcome!

this is a function to float range in python

```python runnable
from itertools import takewhile, count

def floatrange (_start: float, _stop: float = None, _step: float = 1) :
    
    if _stop is None :
        _start, _stop = 0, _start
    for n in takewhile(lambda n:n < _stop, count(_start, _step)):
        yield n

// testing ...
print(list(floatrange(3.5, 10)))
print(list(floatrange(3.5, 10, 0.5)))
```