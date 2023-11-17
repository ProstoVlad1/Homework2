class Pet:
    def __init__(self, name, species):
        self.name = name
        self.species = species
        self.energy = 100

    def sleep(self, hours):
        self.energy += hours * 10
        print(f"{self.name} is sleeping. Energy is {self.energy}.")

    def play(self, hours):
        if self.energy >= hours * 5:
            self.energy -= hours * 5
            print(f"{self.name} is playing. Energy is {self.energy}.")
        else:
            print(f"{self.name} is too tired to play.")

cat = Pet("cookie", "Cat")
cat.sleep(5)
cat.play(3)
 
dog = Pet("bob", "Dog")
dog.sleep(8)
dog.play(4)

