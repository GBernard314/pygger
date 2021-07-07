# Swagger generator
All Objects need to be in ```./Objects```
(for now, **subdirectories** are not handled)

## There is a strict comment convention:
### Chalice route file
```python
@app.route('/pets',  methods=['GET'])
def all_pets():
    """Retrieve all regular pets

    Returns:
        list[Pet]: list of all regular pets
    """
    pets = get_pets(type='regular')
    return pets
```
---
### Classes :
Single class file
```python
class Pet:
    """
    Attributes:
        name (str): pet's name
        age (int): pet's age
        tag (Tag): pet's rfid tag
    """
    def __init__(self, name: str, age: int, tag: Tag):
        self.name = name
        self.age = age
        self.tag = tag
```
Multi class file (_experimental_)
```python
class Pet:
    """ Regular pets
    Attributes:
        name (str): pet's name
        age (int): pet's age
        tag (Tag): pet's rfid tag
    """
    def __init__(self, name: str, age: int, tag: Tag):
        self.name = name
        self.age = type
        self.tag = tag

class Neo_pet:
    """ New kind of pets including snakes, rats etc
    Attributes:
        name (str): pet's name
        age (int): pet's age
        tag (Tag): pet's rfid tag
        size (float): pet's size
    """
    def __init__(self, name: str, age: int, tag: Tag, size: float):
        self.name = name
        self.age = type
        self.tag = tag
        self.size = size
```

## Installation
   ```bash 
   pip install pygger
   ```