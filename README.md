#Burc ve yas hesaplayıcı
import time


def lessonHomework():
    name = str(input("Adınızı giriniz :"))
    surname = str(input("Soyadınızı giriniz :"))
    day = int(input('Doğdugunuz günü giriniz: '))
    month = int(input('Doğdugunuz ayı sayı olarak giriniz: '))
    year = int(input('Doğum yılınızı giriniz: '))
    gender = input("Cinsiyet (Bay için 1 Bayan için 0 )giriniz :") == "1"
    if gender == True:
        gender = "Bay"
    if gender == False:
        gender = "Bayan"
    if ((day > 20) & (month == 1)) or ((day < 16) & (month == 2)):
        horoscop = "Oğlak"
    elif ((day > 16) & (month == 2)) or ((day < 11) & (month == 3)):
        horoscop = "Kova"
    elif ((day > 11) & (month == 3)) or ((day < 18) & (month == 4)):
        horoscop = "Balık"
    elif ((day > 18) & (month == 4)) or ((day < 13) & (month == 5)):
        horoscop = "Koç"
    elif ((day > 13) & (month == 5)) or ((day < 21) & (month == 6)):
        horoscop = "Boğa"
    elif ((day > 21) & (month == 6)) or ((day < 20) & (month == 7)):
        horoscop = "İkizler"
    elif ((day > 20) & (month == 7)) or ((day < 10) & (month == 8)):
        horoscop = "Yengeç"
    elif ((day > 10) & (month == 8)) or ((day < 16) & (month == 9)):
        horoscop = "Aslan"
    elif ((day > 16) & (month == 9)) or ((day < 30) & (month == 10)):
        horoscop = "Başak"
    elif ((day > 30) & (month == 10)) or ((day < 23) & (month == 11)):
        horoscop = "Terazi"
    elif ((day > 23) & (month == 11)) or ((day < 29) & (month == 11)):
        horoscop = "Akrep"
    elif ((day > 29) & (month == 11) or (day < 17) & (month == 12)):
        horoscop = "Yılan"
    elif ((day > 17) & (month == 12) or (day < 20) & (month == 1)):
        horoscop = "Yay"
    d = time.localtime()
    age = (d.tm_year) - (year)
    print(f"{age} yaşındasınız")
    print('Burcunuz: {}'.format(horoscop))

    if len(name) > len(surname):
        print(f"Sayın {gender} {name}isimli kişi {age} yaşındasınız ve burcunuz {horoscop}dır")
    elif len(name) == len(surname):
        print(f"Sayın {gender} {name} ve {surname} soy isimli kişi {age} yaşındasınız ve burcunuz {horoscop}dır")
    elif len(name) < len(surname):
        print(f"Sayın {gender} {surname} soy isimli kişi {age} yaşındasınız ve burcunuz {horoscop}tir")


if __name__ == "__main__":
    lessonHomework()
