port=8000
שם משתנה סביבה: GREETING.
ברירת המחדל: Hello.


# בחירת image בסיס של Python בגרסה מדויקת
FROM python:3.11-slim

# קביעת תיקיית העבודה בתוך הקונטיינר
WORKDIR /app

# העתקת קובץ התלויות לפני העתקת קוד האפליקציה
COPY requirements.txt .

# התקנת התלויות הדרושות להפעלת האפליקציה
RUN pip install --no-cache-dir -r requirements.txt

# העתקת קוד האפליקציה לתוך הקונטיינר
COPY app.py .

# הצהרה שהאפליקציה משתמשת בפורט 8000
EXPOSE 8000

# הפעלת שרת Flask באמצעות צורת exec
CMD ["python", "app.py"]
