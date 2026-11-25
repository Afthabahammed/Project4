# Project4 – Complaint Management System

## About the Project

Project4 is a web-based Complaint Management System developed using Python and Django. It provides a platform for users and faculty to manage complaint-related activities through a web interface.

The application includes user registration, login, complaint submission, and complaint-related management functionality. It was used as one of the applications in my DevSecOps implementation project.

## Technologies Used

- **Python** – Main programming language
- **Django** – Web application framework
- **MySQL** – Database management
- **HTML, CSS and JavaScript** – Frontend development
- **Docker** – Application containerization
- **Jenkins** – CI/CD pipeline automation
- **Semgrep** – Static Application Security Testing (SAST)
- **Trivy** – Dependency vulnerability scanning
- **Amazon ECR** – Docker image storage
- **Kubernetes (K3s)** – Application deployment and orchestration
- **Argo CD** – GitOps-based deployment management
- **OWASP ZAP** – Dynamic Application Security Testing (DAST)

## Application Features

- User registration and login
- Complaint-related functionality
- Faculty-related functionality
- Complaint acknowledgement and management
- Web-based interface for application access

## Running the Application Locally

### 1. Clone the Repository

```bash
git clone https://github.com/Afthabahammed/Project4.git
cd Project4
```

### 2. Install Dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure the Database

Configure the required Django and MySQL environment variables:

- `DJANGO_SECRET_KEY`
- `DB_NAME`
- `DB_HOST`
- `DB_USER`
- `DB_PASSWORD`

### 4. Run Database Migrations

The Django management file is inside the `project4` directory.

```bash
cd project4
python manage.py migrate
```

### 5. Start the Development Server

```bash
python manage.py runserver
```

Open `http://127.0.0.1:8000` in your browser.

## DevSecOps Implementation

As part of this project, I implemented an automated DevSecOps workflow to improve the security, build process, and deployment of the application.

The workflow includes:

1. **Source Code Management:** Application source code is maintained in GitHub.
2. **SAST:** Semgrep is used to scan the source code for potential security issues.
3. **Dependency Scanning:** Trivy checks project dependencies for known vulnerabilities.
4. **CI/CD Pipeline:** Jenkins automates the build and security scanning stages.
5. **Docker:** The application is packaged into a Docker image.
6. **Amazon ECR:** The Docker image is pushed to Amazon Elastic Container Registry.
7. **Kubernetes:** The application is deployed and managed as a Kubernetes workload.
8. **GitOps:** Argo CD monitors the GitOps repository and synchronizes deployment configurations.
9. **DAST:** OWASP ZAP is used to test the running application for potential web security issues.

## Deployment

The application is deployed on a Kubernetes cluster using Docker images stored in Amazon ECR.

Argo CD manages the deployment through a separate GitOps repository. This helps keep application source code and deployment configuration organized independently.

## Project Goal

The main goal of this project was to gain practical experience in integrating security scanning, CI/CD automation, containerization, cloud image storage, Kubernetes deployment, and GitOps into a single application delivery workflow.
