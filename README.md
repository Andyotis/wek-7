# ----------------------------
# Assignment 1: Superhero Class
# ----------------------------

class Superhero:
    def __init__(self, name, power, universe):
        self.name = name
        self.power = power
        self.universe = universe

    def introduce(self):
        print(f"I am {self.name} from the {self.universe} universe, and I can {self.power}!")

    def attack(self):
        print(f"{self.name} uses their superpower: {self.power} 💥")

# Inherited class
class FlyingSuperhero(Superhero):
    def __init__(self, name, power, universe, flight_speed):
        super().__init__(name, power, universe)
        self.flight_speed = flight_speed

    def attack(self):  # Polymorphism: method overridden
        print(f"{self.name} soars through the sky at {self.flight_speed} km/h and uses {self.power} ✈️")


# ----------------------------
# Activity 2: Polymorphism Challenge with Animals
# ----------------------------

class Animal:
    def move(self):
        print("This animal moves somehow.")

class Dog(Animal):
    def move(self):
        print("Dog runs 🐕")

class Bird(Animal):
    def move(self):
        print("Bird flies 🐦")

class Fish(Animal):
    def move(self):
        print("Fish swims 🐟")


# ----------------------------
# TESTING THE PROGRAM
# ----------------------------

print("🦸‍♂️ Superhero Example:")
hero1 = Superhero("Flash", "run at the speed of light", "DC")
hero2 = FlyingSuperhero("Iron Man", "shoot repulsor beams", "Marvel", 1200)

hero1.introduce()
hero1.attack()
hero2.introduce()
hero2.attack()

print("\n🐾 Animal Movement Example:")
animals = [Dog(), Bird(), Fish()]
for animal in animals:
    animal.move()
