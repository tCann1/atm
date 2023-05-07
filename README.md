# atm
print("""

Bait ATM Makinesi 
İşlemler:

1. Bakiye Sorgulama
2. Para Yatırma
3. Para Çekme

İşlemi sonlandırmak için '0'ı tuşlayın.
""")

bakiye = 10000

while True:
    işlem = input("İşlem Numarası: ")
    
    if (işlem=="0"):
        print("İşlem Sonlandırıldı")
        break
    elif (işlem == "1"):
        print("Toplam bakiye={}".format(bakiye))
        
    elif (işlem =="2"):
        tutar = int(input("Yatırılmak istenilen tutar:"))
        bakiye += tutar
        
    elif (işlem =="3"):
        tutar = int(input("Çekmek istenilen tutar:"))
        if (bakiye - tutar < 0):
            print("Yetersiz Bakiye")
            continue
        bakiye -= tutar
        
        
    else:
        print("Onaylanmayan İşlem")  
