# IBM Back-End Development Capstone: Online Course Platform

This repository contains the Capstone Project developed as part of the **IBM Back-End Development Professional Certificate** program on Coursera.

The project is a fully functional Django-based Learning Management System (LMS) where users can browse courses, enroll in them, and take final exams.

## 🎓 About the Certification

This project is the culmination of a comprehensive 11-course program by IBM Skills Network, covering the entire back-end development lifecycle:

* Python and Django Web Framework
* SQL and Databases
* Containers (Docker, Kubernetes, OpenShift)
* Microservices and Serverless Architecture
* Application Security, Monitoring, and Linux/Git workflows

## ✨ Key Features

* **User Authentication:** Registration, login, and logout functionality.
* **Course Catalog:** View available courses sorted by popularity and explore course materials (lessons).
* **Enrollment System:** Users can enroll in specific courses.
* **Examination Module:** * Take an exam upon course completion.
  * Automated grading system (strict scoring: points for a question are awarded only if the selected choices match the correct answers 100%).
  * Instant score calculation and result display.
* **Admin Panel:** Content management (courses, lessons, questions, and choices) via the built-in Django admin interface.

## 🛠 Tech Stack

* **Backend:** Python, Django 4.2.3
* **Frontend:** HTML5, CSS3, Bootstrap (Server-Side Rendering via Django templates)
* **Database:** SQLite (default configuration)
* **Server:** Gunicorn 20.1.0

## ☁️ Cloud Deployment Architecture (Cloud Foundry)

The project is designed for Platform-as-a-Service (PaaS) deployment using a two-component architecture (as configured in `manifest.yml`):

1. **Main Application (`onlinecourse`):** The Python backend handling business logic.
2. **Static Server (`onlinecourse-nginx`):** An Nginx server using `staticfile_buildpack`, optimized for serving static assets (CSS, JS, images).

## 🚀 Running Locally

1. Clone the repository:

   ```bash
   git clone <YOUR_REPOSITORY_URL>
   ```

2. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

3. Run database migrations:

    ```bash
    python manage.py makemigrations
    python manage.py migrate
    ```

4. Create a superuser for the admin panel:

    ```bash
    python manage.py createsuperuser
    ```

5. Start the development server:

    ```bash
    python manage.py runserver
    ```

6. Open `http://localhost:8000` in your browser (Admin panel is at `http://localhost:8000/admin`).

---

**General Notes**

An `onlinecourse` app has already been provided in this repo upon which you will be adding a new assesement feature.

* If you want to develop the final project on Theia hosted by [IBM Developer Skills Network](https://labs.cognitiveclass.ai/), you will need to create the same project structure on Theia workspace and save it everytime you close the browser
* Or you could develop the final project locally by setting up your own Python runtime and IDE
* Hints for the final project are left on source code files
* You may choose any cloud platform for deployment (default is IBM Cloud Foundry)
* Depends on your deployment, you may choose any SQL database Django supported such as SQLite3, PostgreSQL, and MySQL (default is SQLite3)

**ER Diagram**
For your reference, we have prepared the ER diagram design for the new assesement feature.

![Onlinecourse ER Diagram](https://github.com/ibm-developer-skills-network/final-cloud-app-with-database/blob/master/static/media/course_images/onlinecourse_app_er.png)
