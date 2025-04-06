# Week5-Assigment
this is Week5 assignment
# SMARTHONE

# Parent Class
class Smartphone:
    def __init__(self, brand, model, storage):
        self.brand = brand
        self.model = model
        self.__storage = storage  # Encapsulated attribute

    def make_call(self, number):
        print(f"{self.model} is calling {number}...")

    def get_storage(self):
        return self.__storage

    def add_storage(self, extra):
        self.__storage += extra
        print(f"Storage increased to {self.__storage}GB")

# Subclass - Inheritance
class GamingPhone(Smartphone):
    def play_game(self, game_name):
        print(f"Playing {game_name} on {self.model} with smooth graphics! 🎮")

# Creating an object
phone1 = GamingPhone("ASUS", "ROG Phone 5", 128)
phone1.make_call("123-456-789")
phone1.play_game("PUBG Mobile")
phone1.add_storage(64)
print("Total storage:", phone1.get_storage())

# VIECHLES

class Vehicle:
    def move(self):
        print("This vehicle moves.")

class Car(Vehicle):
    def move(self):
        print("Driving 🚗")

class Plane(Vehicle):
    def move(self):
        print("Flying ✈️")

class Boat(Vehicle):
    def move(self):
        print("Sailing 🚢")

# Polymorphism in action
vehicles = [Car(), Plane(), Boat()]

for v in vehicles:
    v.move()




