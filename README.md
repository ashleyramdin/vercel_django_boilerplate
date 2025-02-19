# 🚀 Vercel Django Boilerplate

A minimal **Django 5.1** boilerplate configured for deployment on **Vercel**. This template provides an easy way to deploy Django projects with serverless functions.

## 📌 Features

- ✅ **Django 5.1** setup  
- ✅ **Vercel deployment** ready  
- ✅ Configured for **serverless functions**  
- ✅ **SQLite (default)** or any database support  
- ✅ **Environment variables** via `.env`  or the Vercel dashboard

## 📂 Project Structure

```
vercel_django_boilerplate/
│── api/                # Main Django app
│   ├── settings.py     # Django settings
│   ├── urls.py         # URL routing
│   ├── wsgi.py         # WSGI app entry point
│   ├── asgi.py         # ASGI app entry point (if using ASGI)
│
│── core/               # Example Django app
│── templates/          # Template files (if needed)
│── manage.py           # Django CLI
│── server.py           # Required for Vercel deployment
│── requirements.txt    # Dependencies
│── vercel.json         # Vercel configuration
│── .env.example        # Example environment variables
│── README.md           # Project documentation
```

## 🚀 Deployment on Vercel

### **1️⃣ Install Vercel CLI**  
```sh
npm install -g vercel
```

### **2️⃣ Login to Vercel**
```sh
vercel login
```

### **3️⃣ Deploy the App**
```sh
vercel
```

## 🛠️ Development Setup

1. Clone the repository:  
   ```sh
   git clone https://github.com/yourusername/vercel_django_boilerplate.git
   cd vercel_django_boilerplate
   ```

2. Create a virtual environment:  
   ```sh
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:  
   ```sh
   pip install -r requirements.txt
   ```

4. Set up environment variables:  
   - Copy `.env.example` to `.env` and update the values.

5. Run the Django development server:  
   ```sh
   python manage.py runserver
   ```

## 🌎 Environment Variables

The project uses a `.env` file to store environment variables for running locally. Example:

```
DEBUG=True
SECRET_KEY=your-secret-key
DATABASE_URL=sqlite:///db.sqlite3

```

On Vercel dashboard for your project, you can go to Project Settings/Environment Variables to configure key-value pairs for the different environments. You can then configure them in the settings.py using:
```
import os
MY_SECRET_KEY = os.environ.get('MY_SECRET_KEY')
```


## 📜 License

This project is **open-source** and available under the **MIT License**.

---

This README should provide a solid foundation for your GitHub repository! 🚀 Let me know if you'd like any modifications.