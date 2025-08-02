def kalkulator():
    print("Jednostavan kalkulator")
    print("Odaberite operaciju:")
    print("1. Zbrajanje")
    print("2. Oduzimanje")
    print("3. Množenje")
    print("4. Dijeljenje")
    
    izbor = input("Unesite broj operacije (1/2/3/4): ")
    
    broj1 = float(input("Unesite prvi broj: "))
    broj2 = float(input("Unesite drugi broj: "))
    
    if izbor == '1':
        print(f"{broj1} + {broj2} = {broj1 + broj2}")
    elif izbor == '2':
        print(f"{broj1} - {broj2} = {broj1 - broj2}")
    elif izbor == '3':
        print(f"{broj1} * {broj2} = {broj1 * broj2}")
    elif izbor == '4':
        if broj2 != 0:
            print(f"{broj1} / {broj2} = {broj1 / broj2}")
        else:
            print("Dijeljenje s nulom nije dozvoljeno!")
    else:
        print("Neispravan unos operacije!")

if __name__ == "__main__":
    kalkulator()
