# 📸 Image Upload Web Application (Django)

A simple Django-based web application that allows users to upload, store, and display images. This project demonstrates how to handle media files in Django and render them dynamically on the frontend.

---

## 🚀 Features

* Upload images through a web form
* Store images using Django `ImageField`
* Display uploaded images dynamically
* Handle missing images gracefully
* Clean and simple UI

---

## 🛠️ Tech Stack

* **Backend:** Python, Django
* **Frontend:** HTML, CSS, Bootstrap
* **Database:** SQLite
* **Media Handling:** Django Media Files

---

## 📂 Project Setup

### 🔹 1. Clone the Repository

```bash
git clone https://github.com/your-username/your-repo-name.git
cd your-repo-name
```

---

### 🔹 2. Create Virtual Environment

```bash
python -m venv venv
```

#### Activate Environment:

* **Windows:**

```bash
venv\Scripts\activate
```

* **Mac/Linux:**

```bash
source venv/bin/activate
```

---

### 🔹 3. Install Dependencies

```bash
pip install -r requirements.txt
```

> If `requirements.txt` is not available:

```bash
pip install django pillow
```

---

### 🔹 4. Apply Migrations

```bash
python manage.py makemigrations
python manage.py migrate
```

---

### 🔹 5. Create Superuser (Optional)

```bash
python manage.py createsuperuser
```

---

### 🔹 6. Run Development Server

```bash
python manage.py runserver
```

Open your browser and go to:

```
http://127.0.0.1:8000/
```

---

## 📁 Media Configuration (Important)

Make sure your `settings.py` has:

```python
MEDIA_URL = '/media/'
MEDIA_ROOT = os.path.join(BASE_DIR, 'media')
```

And in your main `urls.py`:

```python
from django.conf import settings
from django.conf.urls.static import static

urlpatterns = [
    # your paths
] + static(settings.MEDIA_URL, document_root=settings.MEDIA_ROOT)
```

---

## 📸 How It Works

1. User uploads an image via form
2. Image is stored in the `media/` folder
3. File path is saved in the database
4. Images are rendered dynamically in templates

---

## 📌 Future Improvements

* User authentication (login/signup)
* Image validation and compression
* Drag-and-drop upload UI
* Cloud storage integration (AWS S3 / Cloudinary)

---

## 🤝 Contributing

Feel free to fork this repo and submit pull requests.

---

## 📄 License

This project is open-source and available under the MIT License.
