
Proje Adı: Kod Asistanım (kod_asistanim)
Açıklama: 9. Sınıf Programlama Temelleri dersi için hazırlanan temel Python uygulaması.
"""

def karsilama_yap(kullanici_adi):
    """Kullanıcıya hoş geldin mesajı verir."""
    print(f"========================================")
    print(f"  Merhabalar, {kullanici_adi}! Projeye Hoş Geldin.")
    print(f"========================================")

def ortalama_hesapla(not1, not2, not3):
    """Girilen 3 notun ortalamasını hesaplar ve geçme durumunu söyler."""
    ortalama = (not1 + not2 + not3) / 3
    print(f"\n[Not Hesaplama Modülü]")
    print(f"Girilen Notlar: {not1}, {not2}, {not3}")
    print(f"Ortalama: {ortalama:.2f}")
    
    if ortalama >= 50:
        print("Durum: Geçti 🥳")
    else:
        print("Durum: Kaldı 📚")

def sayi_tahmin_ipucu(gizli_sayi, tahmin):
    """Basit bir sayı karşılaştırma mantığı."""
    print(f"\n[Sayı Tahmin Modülü]")
    print(f"Tahmin Edilen Sayı: {tahmin}")
    if tahmin == gizli_sayi:
        print("Tebrikler! Doğru tahmin.")
    elif tahmin < gizli_sayi:
        print("İpucu: Daha *büyük* bir sayı dene.")
    else:
        print("İpucu: Daha *küçük* bir sayı dene.")

# Ana Çalıştırma Alanı
if __name__ == "__main__":
    # 1. Karşılama Fonksiyonu
    karsilama_yap("Öğrenci")
    
    # 2. Not Ortalaması Örneği
    ortalama_hesapla(70, 85, 90)
    
    # 3. Sayı Tahmin Örneği
    sayi_tahmin_ipucu(42, 35)
