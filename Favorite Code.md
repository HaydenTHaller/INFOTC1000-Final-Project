# My Favorite Code so Far

**Animal Class Assignment from IT1400:**

Animal Class:
```python
from Animal import Animal

print('Welcome to the animal generator!')

print('This program creates Animal Objects.')

def main():
    again = 'y'

    animal_list = []

    while again == 'y':
        animal_type = input('What type of animal would you like to create? ')
        name = input("What is the animal's name? ")

        animal = Animal(animal_type, name)

        animal_list.append(animal)

        again = input('Would you like to create another animal? (y/n): ')

    for item in animal_list:
        print(item.get_name() + ' the ' + item.get_animal_type() + ' is ' + item.check_mood() + '.')

main()
```

Animals.py:
```python
import random

class Animal:
    def __init__(self, animal_type, name):
        self.__animal_type = animal_type
        self.__name = name
        self.__mood = 'happy'

    def check_mood(self):
        if random.randint(1,3) == 1:
            self.__mood = 'happy'
        elif random.randint(1,3) == 2:
            self.__mood = 'hungry'
        else:
            self.__mood = 'sleepy'
        return self.__mood

    def get_animal_type(self):
        return self.__animal_type

    def get_name(self):
        return self.__name
    
```
**FizzBuzz IT1000:**
```html
<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<title>Fizz Buzz</title>
<script>

function fizzbuzz() {
	var display = document.getElementById('display');
	var displayHTML = "";
	for (i = 1; i < 101; i++) {
        if (i % 3 == 0 && i % 5 == 0) {
            displayHTML += '<p>' + 'FizzBuzz' + '</p>' }
        else if (i % 3 == 0) {
            displayHTML += '<p>' + 'Fizz' + '</p>' }
        else if (i % 5 == 0) {
            displayHTML += '<p>' + 'Buzz' + '</p>' }
        else {
		displayHTML += "<p>" + i + "</p>"; }
	}
	display.innerHTML = displayHTML
}

</script>

</head>

<body onload="fizzbuzz()">
<div id="display">

</div>
</body>

</html>
```
