# Imagen base liviana
FROM python:3.12-slim

# Instalar dependencias necesarias
RUN apt-get update && apt-get install -y build-essential && apt-get clean

# Crear directorio de trabajo
WORKDIR /app

# Copiar requirements y entorno
COPY requirements.txt ./
RUN pip install --no-cache-dir -r requirements.txt

# Copiar archivos del bot
COPY bot.py ./
COPY .env ./

# Comando para iniciar el bot
CMD ["python", "bot.py"]
