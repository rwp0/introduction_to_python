## The self parameter

It's time to explain the `self` parameter we saw in previous tasks.
The first argument passed to a class method is `self`. This is nothing more 
than a convention: the name `self` has no special meaning to Python. 
It is advised to follow the convention, otherwise your code may be less readable 
to other Python programmers.

Python will use the `self` parameter to refer to the object being created.  
Methods may call other methods by using method attributes of the `self` argument:

```python
class Bag:
    def __init__(self):
        self.data = []

    def add(self, x):
        self.data.append(x)

    def addtwice(self, x):
        self.add(x)
        self.add(x)
```
  
In the code editor, implement the `add` method. It should add `amount` to 
the `current` field.  

<div class='hint'>Add <code>amount</code> to the <code>self.current</code> variable.</div>
<div class="hint">Use the <code>+=</code> sign.</div>