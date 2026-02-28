Provide as an overview for those who are interested.

1. Project Structure
   Project has the following layout (relative to the Dockerfile):

sonarr-calendar/
├── src/
│ └── sonarr_calendar/
│ ├── **init**.py
│ ├── **main**.py
│ ├── cli.py
│ ├── config.py
│ ├── api_client.py
│ ├── models.py
│ ├── image_cache.py
│ ├── html_generator.py
│ ├── utils.py
│ └── templates/
│ └── calendar.html.j2
├── requirements.txt
├── setup.py (optional, not needed for container)
├── Dockerfile
├── docker-compose.yml
├── .dockerignore
└── README.md

############################################################### 2. Create a .dockerignore File
Hopefully this keeps the image small by excluding unnecessary files.

.git
**pycache**
_.pyc
_.pyo
.pytest_cache
.coverage
htmlcov
sonarr_images
sonarr_calendar.html
sonarr_calendar_data.json
README.md

############################################################### 3. Create the Dockerfile
