# Tarmoq Xavfsizligi Monitoring Tizimi

Sun'iy intellekt asosida real vaqtda tarmoq xavfsizligini kuzatish dasturi.

## Lokal ishga tushirish (o'z kompyuteringizda)

```bash
# 1. Kutubxonalarni o'rnatish
pip install -r requirements.txt

# 2. Dasturni ishga tushirish
python app.py

# 3. Brauzerda ochish
# http://localhost:5000
```

## Render.com ga joylash (bepul, doim online)

1. https://github.com ga kiring va yangi repository yarating
2. Barcha fayllarni yuklang
3. https://render.com ga kiring (bepul ro'yxatdan o'ting)
4. "New Web Service" tugmasini bosing
5. GitHub repository ni ulang
6. Sozlamalar:
   - Build Command: `pip install -r requirements.txt`
   - Start Command: `gunicorn --worker-class eventlet -w 1 app:app`
7. "Deploy" tugmasini bosing
8. 2-3 daqiqadan keyin sizga link beriladi

## Loyiha tuzilmasi

```
network_monitor/
├── app.py              # Python backend (Flask + SocketIO)
├── requirements.txt    # Kutubxonalar
├── Procfile           # Server sozlamalari
└── templates/
    └── index.html     # Dashboard interfeysi
```

## Imkoniyatlar

- Real vaqtda tarmoq trafigi kuzatuvi
- AI asosida anomaliya aniqlash
- DDoS, Port scan, Brute-force, Fishing hujumlarini aniqlash
- WebSocket orqali jonli yangilanish
- Hujum simulyatsiyasi
