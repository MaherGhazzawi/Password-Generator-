# 🔐 PyPassword Generator – Dein eigener Passwort-Zauberer in Python

Willkommen zu meinem kleinen Projekt, das in einem Udemy-Kurs entstanden ist:  
Ein Passwort-Generator, der sicher ist – und dabei **dir die volle Kontrolle** lässt.  
Ob einfache Passwörter oder wilde Zeichenkombinationen – du bestimmst, was drin steckt.

## ✨ Features

- Wähle die genaue Anzahl von:
  - Groß- und Kleinbuchstaben
  - Symbolen (`!`, `#`, `$`, usw.)
  - Zahlen (0–9)
- Zwei Passwort-Modi:
  - **Einfach**: Zeichen in der gewählten Reihenfolge
  - **Schwer**: Zeichen vollständig durchmischt für mehr Sicherheit
- Keine String-Module – **bewusst manuell**, um zu lernen
- `random.sample()` für Auswahl, `random.shuffle()` für Chaos

## 📦 Installation

Hier ist meinen Code : 
#Password Generator Project
import random
letters = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z', 'A', 'B', 'C', 'D', 'E', 'F', 'G', 'H', 'I', 'J', 'K', 'L', 'M', 'N', 'O', 'P', 'Q', 'R', 'S', 'T', 'U', 'V', 'W', 'X', 'Y', 'Z']
numbers = ['0', '1', '2', '3', '4', '5', '6', '7', '8', '9']
symbols = ['!', '#', '$', '%', '&', '(', ')', '*', '+']

print("Welcome to the PyPassword Generator!")
nr_letters= int(input("How many letters would you like in your password?\n")) 
nr_symbols = int(input(f"How many symbols would you like?\n"))
nr_numbers = int(input(f"How many numbers would you like?\n"))

#Eazy Level - Order not randomised:
#e.g. 4 letter, 2 symbol, 2 number = JduE&!91
choice_of_letters = random.sample(letters,nr_letters)
choice_of_symbols = random.sample(symbols,nr_symbols)
choice_of_number = random.sample(numbers,nr_numbers)
password_list = choice_of_symbols + choice_of_letters + choice_of_number
easy_password = "".join(password_list)
print(f"Easy Password is : {easy_password}")


#Hard Level - Order of characters randomised:
#e.g. 4 letter, 2 symbol, 2 number = g^2jk8&P
choice_of_letters = random.sample(letters,nr_letters)
choice_of_symbols = random.sample(symbols,nr_symbols)
choice_of_number = random.sample(numbers,nr_numbers)
password_list = choice_of_symbols + choice_of_letters + choice_of_number
random.shuffle(password_list)
password = "".join(password_list)
print(f"This is your hard Password : {password}")

