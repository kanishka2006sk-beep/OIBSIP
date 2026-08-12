import requests

city = input("Enter city name: ").strip()

if city == "":
    print("City name cannot be empty.")
    exit()

try:
    url = f"https://wttr.in/{city}?format=j1"
    response = requests.get(url, timeout=10)

    if response.status_code != 200:
        print("Unable to fetch weather data.")
        exit()

    data = response.json()

    current = data["current_condition"][0]

    temp_c = current["temp_C"]
    temp_f = current["temp_F"]
    humidity = current["humidity"]
    wind = current["windspeedKmph"]
    condition = current["weatherDesc"][0]["value"]

    print("\n------ Weather Report ------")
    print("City:", city.title())
    print("Temperature:", temp_c, "°C")
    print("Temperature:", temp_f, "°F")
    print("Humidity:", humidity + "%")
    print("Condition:", condition)
    print("Wind Speed:", wind, "km/h")

except requests.exceptions.RequestException:
    print("Network Error! Please check your internet connection.")
except Exception:
    print("Invalid city name or weather data not available.")
