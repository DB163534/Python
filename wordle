import random

# Baza slow
words = ['dom', 'negatyw', 'komputer', 'ciasto',
         'narciarz', 'wypoczynek', 'apteka', 'artysta',
         'basen', 'bokser', 'burmistrz', 'kobieta', 'morze', 'picie', 'pisarz', 'policja', 'praca', 'prokurator', 'przedszkolak', 'rower', 'samolot', 'srebro']
 
# Losowanie slowa
word = random.choice(words)
 
print("Zgadnij slowo: ")
 
guesses = ''
 
# Liczba tur
turns = 12
 
 
while turns > 0:
 
    failed = 0
 
    # Slowa po kolei
    for char in word:
 
        # Sprawdzanie poprawnosci 
        if char in guesses:
            print(char, end=" ")
        else:
            print("_", end=" ")
            failed += 1
            
    if failed == 0:
        print("")
        print("Wygrales!")
 
        # Wypisywanie poprawnego slowa
        print("Slowo to: ", word)
        break
 
    # Prosba o nowa litere
    print()
    guess = input("Zgadnij litere: ")
    
    if guess in guesses:
        print("Ta litera byla juz zgadywana")
    else:
        # Zapisywanie zgadniec
        guesses += guess

        if guess not in word:
            turns -= 1
            print("Zle")
 
            if turns > 0:
                if turns > 4:
                    print("Masz jeszcze", + turns, 'prob')
                if turns < 5 and turns > 1:
                    print("Masz jeszcze", + turns, "proby")
                if turns == 1:
                    print("Zostala ci ostatnia proba!")
            else:
                print("Przegrales")
