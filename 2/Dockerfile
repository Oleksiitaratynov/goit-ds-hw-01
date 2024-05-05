# Use an official Python runtime as the base image
FROM python:3.12


# Встановимо змінну середовища
ENV APP_HOME /app

# Set the working directory in the container
WORKDIR /app

# Copy the poetry.lock and pyproject.toml files
COPY . .

# Install Poetry
RUN pip install poetry

# Install dependencies using Poetry
RUN pip install -r requirements.txt

#COPY personal_assistant.py /app/
COPY . /app

# Make port 3000 available to the world outside this container
EXPOSE 5000

# Запустимо наш застосунок всередині контейнера
ENTRYPOINT ["python", "bot.py"]
