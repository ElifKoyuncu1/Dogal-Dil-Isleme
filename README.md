# DOĞAL DİL İŞLEME PROJESİ

Bu projede Amazon yorumlarını doğal dil işleme teknikleriyle geliştirerek daha verimli ürün önerileri oluşturmayı hedefliyorum.

## Gerekli Kütüphaneler ve Kurulum Talimatları

`pip install pandas` 

`pip install nltk`

`pip install gensim`

`pip install matplotlib`

`pip install scikit_learn`

## Veri Seti Hakkında

Proje kapsamında kullanılan veri seti, Amazon ürün yorumlarını içermektedir. Veri seti aşağıdaki amaçlar için kullanılabilir:

* Müşteri yorumlarından ürün hakkında anlam çıkarma

* Yorumları olumlu/olumsuz olarak sınıflandırma (sentiment analysis)

* Kelime ilişkilendirme (Word2Vec ile)

* Ürün geliştirme için öneriler çıkarma

 ## Modelin Oluşturulması

1. **Veri Setinin Yüklenmesi:**

* pandas ile CSV formatındaki veri seti yüklenir.

* Yorum metni sütunu analiz için seçilir.

2. **Ön İşleme:**

* Küçük harfe çevirme

* Noktalama işaretlerinin kaldırılması

* Stop words temizliği (nltk kullanılarak)

* Tokenization işlemi

3. **Lemmatizasyon ve Stemming:**

* Temizlenmiş ve tokenlenmiş yorumlar lemmatize edilip csv dosyasına kaydedilir.

* Temizlenmiş ve tokenlenmiş yorumlar stemize edilir ve csv dosyasına kaydedilir.

4. **TF-IDF vektörleştirme:**

* Oluşturulan lemma ve stem dosyaları TF-IDF ile vektörize edilir.

5. **Model Eğitimi (Word2Vec):**

* gensim.models.Word2Vec sınıfı ile eğitim yapılır.

* Parametreler (window, vector_size vs.) belirlenir.

* Model kaydedilir (.model veya .bin olarak)

* Lemma ve stem dosyaları için ayrı ayrı modeller kullanılır. 
