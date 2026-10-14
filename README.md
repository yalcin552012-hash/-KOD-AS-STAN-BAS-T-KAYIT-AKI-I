# Proje Yazarı:Yalçın arslan
# Projenin Adı: Kod-Asistan v0.1
# Ders: Programlama Temelleri

def hesapla():
    """1: Hesap Makinesi İşlevi"""
    print("\n--- HESAP MAKİNESİ MODÜLÜ ---")
    try:
        sayi1 = float(input("1. Sayıyı giriniz: "))
        sayi2 = float(input("2. Sayıyı giriniz: "))
        islem = input("Yapmak istediğiniz işlem (+, -, *, /): ")
        
        if islem == "+":
            print(f"Sonuç: {sayi1 + sayi2}")
        elif islem == "-":
            print(f"Sonuç: {sayi1 - sayi2}")
        elif islem == "*":
            print(f"Sonuç: {sayi1 * sayi2}")
        elif islem == "/":
            if sayi2 != 0:
                print(f"Sonuç: {sayi1 / sayi2}")
            else:
                print("Hata: Bir sayı sıfıra bölünemez!")
        else:
            print("Geçersiz işlem seçimi!")
    except ValueError:
        print("Hata: Lütfen geçerli bir sayı giriniz!")

def oyna():
    """2: Sayı Tahmini İşlevi"""
    print("\n--- SAYI TAHMİN MODÜLÜ ---")
    gizli_sayi = 7
    try:
        tahmin = int(input("1 ile 10 arasında bir sayı tahmin ediniz: "))
        if tahmin == gizli_sayi:
            print("Tebrikler! Doğru tahmin ettiniz. 🎉")
        else:
            print(f"Maalesef yanlış. Doğru sayı {gizli_sayi} olmalıydı.")
    except ValueError:
        print("Hata: Lütfen bir tam sayı giriniz!")

def ana_program():
    """Sözde Koddaki Akış Mantığı (KRİTİK EŞİK)"""
    print("==========================================")
    print("      KOD-ASİSTAN v0.1 ÇALIŞTIRILDI       ")
    print("==========================================")
    
    kullanici_giris = input("Kullanıcı adınızı giriniz: ").strip()
    
    # EĞER KULLANICI_GIRIS boş değilse:
    if kullanici_giris != "":
        print(f"\nHoş geldin, {kullanici_giris}!")
        print("1: Hesap Makinesi")
        print("2: Sayı Tahmini")
        
        islem = input("Lütfen yapacağınız işlemi seçiniz (1/2): ").strip()
        
        if islem == "1":
            hesapla()
        elif islem == "2":
            oyna()
        else:
            print("Geçersiz seçim!")
    else:
        print("Hata: Kullanıcı adı boş bırakılamaz!")

if __name__ == "__main__":
    ana_program()

