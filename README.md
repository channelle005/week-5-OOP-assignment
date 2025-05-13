# week-5-OOP-assignment

Assignment 1: Design Your Own Class! 🏗️
Create a class representing anything you like (a Smartphone, Book, or even a Superhero!).

class Superhero:
    def __init__(self, name, power, city):
        self.name = name
        self.power = power
        self.city = city

    def introduce(self):
        print(f"I am {self.name}, protector of {self.city}!")

    def use_power(self):
        print(f"{self.name} uses {self.power} to fight crime!")

Add attributes and methods to bring the class to life!

class Sidekick(Superhero):
    def __init__(self, name, power, city, mentor):
        super().__init__(name, power, city)
        self.mentor = mentor

    def assist(self):
        print(f"{self.name} assists {self.mentor} in battle!")

Use constructors to initialize each object with unique values.

# Creating a Superhero object
hero = Superhero("Captain Code", "Bug Blasting", "Pythonville")
hero.introduce()
hero.use_power()

print()  # Line break

# Creating a Sidekick object
sidekick = Sidekick("Debug Boy", "Syntax Vision", "Pythonville", "Captain Code")
sidekick.introduce()
sidekick.use_power()
sidekick.assist()

Add an inheritance layer to explore polymorphism or encapsulation.

class Superhero:
    def __init__(self, name, power, city):
        self.__name = name              # Encapsulated (private attribute)
        self._power = power             # Protected (can be accessed by subclasses)
        self.city = city                # Public

    def introduce(self):
        print(f"I am {self.__name}, protector of {self.city}!")

    def use_power(self):
        print(f"{self.__name} uses {self._power} to fight crime!")

    # Encapsulated getter
    def get_name(self):
        return self.__name

    # Encapsulated setter
    def set_name(self, new_name):
        if new_name:
            self.__name = new_name
        else:
            print("Name cannot be empty.")
