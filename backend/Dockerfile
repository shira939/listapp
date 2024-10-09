# בוחרים את התמונה הבסיסית של Python
FROM python:3.10

# הגדרת תיקיית העבודה
WORKDIR /usr/src/app

# העתקת requirements.txt לתוך המיכל
COPY requirements.txt ./

# עדכון pip לגרסה האחרונה
RUN python -m pip install --upgrade pip

# התקנה של certifi
RUN pip install --no-cache-dir --trusted-host pypi.org --trusted-host files.pythonhosted.org certifi

# התקנת התלויות מתוך requirements.txt עם Trusted Host
RUN pip install --no-cache-dir --trusted-host pypi.org --trusted-host files.pythonhosted.org -r requirements.txt

# פתיחת הפורט 3001
EXPOSE 3001

# הפעלת השרת
CMD [ "python", "./src/server.py" ]
