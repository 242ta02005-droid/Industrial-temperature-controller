# Industrial-temperature-controller
# Industrial Temperature Controller

print("INDUSTRIAL TEMPERATURE CONTROLLER")
print("---------------------------------")

set_temperature = 70
heater = False

while True:
    temperature = float(input("\nEnter current temperature (°C): "))

    if temperature < set_temperature - 2:
        heater = True
        print("Temperature: LOW")
        print("Heater: ON")

    elif temperature >= set_temperature:
        heater = False
        print("Temperature: HIGH/SET")
        print("Heater: OFF")

    else:
        print("Temperature: NORMAL")
        print("Heater:", "ON" if heater else "OFF")

    print("Current Temperature:", temperature, "°C")
    print("Set Temperature:", set_temperature, "°C")

    choice = input("\nCheck again? (yes/no): ")

    if choice.lower() != "yes":
        print("\nTemperature controller stopped.")
        break
