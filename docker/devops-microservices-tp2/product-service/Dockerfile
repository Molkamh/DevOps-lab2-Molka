# On utilise une image de base Python légère
FROM python:3.9-slim

# On définit le dossier de travail dans le conteneur
WORKDIR /app

# On copie les dépendances et on les installe
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# On copie le reste du code de l'application
COPY app.py .

# On expose le port sur lequel l'application va tourner
EXPOSE 8001

# La commande pour lancer l'application (basée sur ton fichier app.py)
CMD ["uvicorn", "app:app", "--host", "0.0.0.0", "--port", "8001"]