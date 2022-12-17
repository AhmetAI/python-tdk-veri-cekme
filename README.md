## **Python'da Selenium Kütüphanesi ile https://sozluk.gov.tr/ Sitesinden Veri Çekme**

Bu programda yazdığımız kelimenin Türkçe bir anlamı olup olmadığını anlamak için  https://sozluk.gov.tr/ sitesinden yazdığımız kelimeyi aratıp eğer böyle bir türkçe kelime var ise anlamını ekrana yazdırmamıza yarıyor.

## **Programın Çalışması İçin Gerekli Programı Kurun**
Programın çalışması için aşağıdaki linkten chrome sürümünüze uygun olan sürümü kurun ve python dosyanızın olduğu klasöre indirdiğiniz programı zip klasöründen çıkartıp  atın.

https://chromedriver.chromium.org/downloads

## **Eğer Programın Arkaplanda Çalışmasını istemiyorsanız**

```python
options = webdriver.ChromeOptions()
options.add_argument('--headless')
```


Kodunu silin ve

```python
driver = webdriver.Chrome(options=options)

```
Kodunu

```python
driver = webdriver.Chrome()

```
Olarak değiştirin.

#### Not: Projede selenium kütüphanesi kullanıldığı için eş zamanlı olarak siteye girip veriyi çekme işlemi yapılıyor. Bu nedenle bu işlemin hızı internet bağlantı hızınıza göre değişebilir.
