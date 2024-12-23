# DICOM File Upload and Processing App

Этот проект позволяет загружать и обрабатывать файлы DICOM через веб-интерфейс. После загрузки файла DICOM, он обрабатывается, и результат (изображение в формате PNG) отображается на странице. Также предусмотрена возможность обработки изображения с помощью кнопки на интерфейсе.

## Технологии

- FastAPI — для создания API.
- pydicom — для обработки DICOM файлов.
- Pillow — для работы с изображениями.
- jQuery — для обработки загрузки файлов и интерфейса.

## Установка

Для начала работы с проектом выполните следующие шаги:

### 1. Клонировать репозиторий

Скачайте репозиторий на ваш локальный компьютер:

```bash
git clone https://github.com/VadimKirillov/Mosmed_DiaBERT.git
```
### 2. Установить зависимости

Перейдите в директорию с проектом и установите зависимости:

pip install -r requirements.txt

### 3. Запустить сервер
После установки зависимостей, вы можете запустить сервер с помощью команды:

python app/main.py

Это запустит сервер на http://127.0.0.1:8080, и вы сможете открыть веб-интерфейс в браузере.

## Структура проекта
```
yourproject/
│
├── app/        
│   └── main.py      # Основной серверный файл FastAPI
│
├── templates/       # HTML-шаблоны
├── static/         # Статические файлы (CSS, JavaScript)
├── uploads/        # Папка для PNG файлов
├── uploaded_files/ # Папка для DICOM файлов
├── requirements.txt # Файл с зависимостями
└── README.md       # Этот файл
```

## Работа с приложением

1. Загрузка файла DICOM:
   * Перетащите файл DICOM или выберите файл через интерфейс.
   * После успешной загрузки на сервер, изображение будет обработано и сохранено на сервере.
   * Отображается результат обработки (PNG изображение).

2. Обработка изображения:
   * После загрузки файла появляется кнопка "Обработать изображение". Нажмите её для выполнения дальнейших действий с изображением.
   * После нажатия на кнопку "Обработать изображение" будет недолгая загрузка(обработка файла), после чего вас перенаправит на другую страницу, где вы получите результаты.
