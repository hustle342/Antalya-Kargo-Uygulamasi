🛠️ Proje Kurulum ve Çalıştırma Rehberi

Bu rehber, **Antalya Kargo Optimizasyonu Projesi**'nin yerel bilgisayarınızda (Pop!_OS, Windows veya macOS) başarılı bir şekilde çalıştırılması için gereken tüm adımları içermektedir.

## 1. Depoyu Klonlama ve Klasöre Gitme

Öncelikle Git deposunu yerel diskinize indirin ve proje klasörüne girin:

```bash
git clone https://github.com/hustle342/Antalya-Kargo-Uygulamasi.git
cd Antalya-Kargo-Uygulamasi


2. Python Ortamını Hazırlama

Projenin bağımlı olduğu kütüphaneleri (Streamlit, numpy, googlemaps vb.) kurmak için requirements.txt dosyasını kullanın.
Bash

# Bağımlılıkları kur
pip install -r requirements.txt


3. Google Maps API Anahtarını Ayarlama
Güvenlik Klasörünü Oluşturma: Projenin ana dizininde (yani app.py dosyasının yanında) .streamlit adında gizli bir klasör oluşturun:
Bash

mkdir .streamlit

API Dosyasını Oluşturma: .streamlit klasörünün içine secrets.toml adında bir dosya oluşturun. Bu dosyayı terminalde hızlıca oluşturmak için (kendi anahtarınızı yazarak):
Bash

echo '[google_maps]' > .streamlit/secrets.toml
echo 'api_key = "SENIN_GOOGLE_MAPS_API_ANAHTARIN"' >> .streamlit/secrets.toml

Kurulum tamamlandıktan sonra, uygulamayı Streamlit ile çalıştırın:
Bash

streamlit run app.py
