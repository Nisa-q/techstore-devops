# TechStore DevOps Teslim Kontrol Listesi

## Hazır olanlar
- Flask e-ticaret uygulaması
- Dockerfile
- docker-compose.yml
- Jenkinsfile
- SonarQube ayarı
- Prometheus ayarı
- 30 adet birim/entegrasyon testi
- Selenium UI test dosyası
- README
- Test çıktı dosyaları: evidence/test_results.txt ve evidence/coverage_report.txt
- Rapor taslağı: TechStore_DevOps_Teslim_Raporu_Taslak.docx

## Senin bilgisayarında yapılacak minimum işler
1. GitHub'da `techstore-devops` reposu aç.
2. Projeyi repoya push et.
3. Docker Desktop açıkken `docker-compose up -d` çalıştır.
4. Jenkins pipeline'ı oluşturup Build Now çalıştır.
5. SonarQube, Grafana, Jenkins, coverage ekran görüntülerini al.
6. Rapor taslağındaki köşeli parantezli yerleri doldur.

## Çalıştırma komutları
```bash
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python app.py
python -m pytest tests/test_app.py -v
pip install pytest-cov
pytest tests/test_app.py -v --cov=app --cov-report=term-missing
docker build -t techstore-app:latest .
docker-compose up -d
```
