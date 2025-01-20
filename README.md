
class Smartphone:
    """
    A class representing a Smartphone with attributes and methods to describe its behavior.
    """
    def __init__(self, brand, model, storage, battery_life):
        """Constructor to initialize the Smartphone attributes."""
        self.brand = brand
        self.model = model
        self.storage = storage  # in GB
        self.battery_life = battery_life  # in hours
        self.is_on = False

    def power_on(self):
        """Turn the smartphone on."""
        if not self.is_on:
            self.is_on = True
            print(f"{self.brand} {self.model} is now ON.")
        else:
            print(f"{self.brand} {self.model} is already ON.")

    def power_off(self):
        """Turn the smartphone off."""
        if self.is_on:
            self.is_on = False
            print(f"{self.brand} {self.model} is now OFF.")
        else:
            print(f"{self.brand} {self.model} is already OFF.")

    def check_battery(self):
        """Check the remaining battery life."""
        print(f"Battery life: {self.battery_life} hours remaining.")

class Smartwatch(Smartphone):
    """
    A subclass representing a Smartwatch inheriting from Smartphone.
    """
    def __init__(self, brand, model, storage, battery_life, strap_color):
        super().__init__(brand, model, storage, battery_life)
        self.strap_color = strap_color

    def track_steps(self, steps):
        """Simulate step tracking."""
        print(f"{self.brand} {self.model} tracked {steps} steps.")

# Example usage
if __name__ == "__main__":
    my_phone = Smartphone("Tecno", "Camon 30 Premiere", 1000, 24)
    my_watch = Smartwatch("Tecno", "Tecno Watch 2", 16, 48, "Black")

    my_phone.power_on()
    my_phone.check_battery()
    my_phone.power_off()

    my_watch.power_on()
    my_watch.track_steps(10000)
    my_watch.check_battery()
