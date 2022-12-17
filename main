# Arama kutucuğu id'si : tdk-srch-input
# Arama butonu id'si : tdk-search-btn
# Anlam id'si : anlamlar-gts0

import time
from selenium import webdriver

kelime = input("Kelimeyi girin\n")

#Programın arkaplanda çalışmasını sağlıyoruz
options = webdriver.ChromeOptions()
options.add_argument('--headless')


# ChromeDriver tarayıcı nesnesini oluşturuyoruz
driver = webdriver.Chrome(options=options)

# https://sozluk.gov.tr/ sitesini açıyoruz
driver.get('https://sozluk.gov.tr/')

#Arama kutucuğunu buluyoruz ve yazdığımız kelimeyi kutucuğun içine yazdırıyoruz
searchinput = driver.find_element(by='id', value='tdk-srch-input')
searchinput.send_keys(kelime)

#Arama butonunu buluyoruz ve butona tıklıyoruz
search_button = driver.find_element(by='id', value='tdk-search-btn')
search_button.click()

time.sleep(1)

# "bulunan-gts0" id'sini arıyoruz
elements = driver.find_elements(by='id', value='bulunan-gts0')


# Eğer elementler listesi boş ise element yoktur.
if len(elements) == 0:
    print('Böyle Bir Kelime yok')
else:
    print('Böyle Bir Kelime var')

    # Kelimenin anlamlarını alıyoruz ve yazdırıyoruz
    anlamlar = driver.find_element(by='id', value='anlamlar-gts0')
    print(anlamlar.text)



# Tarayıcıyı kapatıyoruz
driver.quit()
