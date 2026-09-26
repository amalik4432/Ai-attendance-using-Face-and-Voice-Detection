# SnapClass

**SnapClass** is an AI-powered classroom attendance management application designed to make attendance faster and easier using face recognition.

The application provides separate interfaces for teachers and students, supports class enrollment through join codes, and uses AI-based face recognition to assist with automated attendance.

## Features

* AI-powered face recognition attendance
* Teacher and student roles
* Student enrollment
* Class join codes
* Automatic student identification
* Automated attendance recording
* Teacher dashboard
* Student dashboard
* Supabase database integration
* Secure password hashing with bcrypt
* QR code generation
* Audio and voice processing support

## Technology Stack

* **Python**
* **Streamlit** — Web application interface
* **NumPy** — Numerical computation
* **Pandas** — Data processing
* **Scikit-learn** — Machine learning utilities
* **Dlib** — Face detection and recognition
* **Face Recognition Models** — Pre-trained face recognition models
* **Supabase** — Backend and database services
* **Bcrypt** — Password hashing
* **Segno** — QR code generation
* **Pillow** — Image processing
* **Librosa** — Audio processing
* **Resemblyzer** — Voice embeddings and speaker representation

## Project Structure

```text
SnapClass/
│
├── src/
│   ├── components/
│   │   ├── dialog_add_photo.py
│   │   ├── dialog_attendance_results.py
│   │   ├── dialog_auto_enroll.py
│   │   ├── dialog_create_subject.py
│   │   ├── dialog_enroll.py
│   │   ├── dialog_share_subject.py
│   │   ├── dialog_voice_attendance.py
│   │   ├── footer.py
│   │   ├── header.py
│   │   └── subject_card.py
│   │
│   ├── database/
│   │   ├── config.py
│   │   └── db.py
│   │
│   ├── pipelines/
│   │   ├── face_pipeline.py
│   │   └── voice_pipeline.py
│   │
│   ├── screens/
│   │   ├── home_screen.py
│   │   ├── student_screen.py
│   │   └── teacher_screen.py
│   │
│   └── ui/
│       └── base_layout.py
│
├── app.py
├── requirements.txt
└── README.md
```

## Installation

### 1. Clone the Repository

```bash
git clone <repository-url>
cd SnapClass
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate the environment.

**Windows:**

```bash
venv\Scripts\activate
```

**Linux/macOS:**

```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

## Configuration

SnapClass uses Supabase for backend and database services.

Configure the required Supabase credentials according to the project's configuration before running the application.

> **Important:** Never commit API keys, passwords, service-role keys, or other sensitive credentials to the repository.

## Running the Application

Start the Streamlit application with:

```bash
streamlit run main.py
```

Streamlit will provide a local URL that can be opened in a web browser.

## User Roles

### Teacher

Teachers can:

* Manage classroom activities
* Manage enrolled students
* Use AI-assisted attendance
* Monitor attendance information
* Manage class enrollment

### Student

Students can:

* Join classes using a join code
* Enroll in classes
* Complete face enrollment
* Access their student interface
* View attendance information

## Face Recognition

SnapClass uses face recognition to identify enrolled students and assist with automated attendance.

The recognition pipeline uses Dlib and pre-trained face-recognition models to generate and compare facial representations.

### Model Accuracy

**Face Recognition Model Accuracy: 99.38% on the LFW benchmark**

For more information, see the [Labeled Faces in the Wild (LFW) paper](https://people.cs.umass.edu/~elm/papers/lfw.pdf).

## Attendance Workflow

```text
Student Enrollment
       │
       ▼
Face Data Collection
       │
       ▼
Face Representation
       │
       ▼
Face Recognition
       │
       ▼
Student Identification
       │
       ▼
Attendance Recording
```

## Join Code Workflow

```text
Teacher Creates Class
        │
        ▼
Class Join Code
        │
        ▼
Student Enters Join Code
        │
        ▼
Student Enrollment
        │
        ▼
Class Membership
```

## Requirements

The main dependencies are listed in `requirements.txt`:

```text
streamlit

# Utilities
numpy
pandas

# Face Recognition
scikit-learn
dlib-bin
git+https://github.com/ageitgey/face_recognition_models
setuptools<70.0.0

# Backend / Authentication
supabase
bcrypt

# QR Code / Image Processing
segno
pillow

# Audio / Voice Processing
librosa
resemblyzer
```

## Security

SnapClass uses:

* **Bcrypt** for password hashing
* **Supabase** for backend and database management
* Environment-based configuration for sensitive credentials

Sensitive credentials should never be committed to Git.

## Future Improvements

* Improved face recognition under different lighting conditions
* Liveness detection
* Attendance analytics and reporting
* More comprehensive system evaluation
* Improved scalability
* Mobile-friendly interface
* Advanced anti-spoofing mechanisms

## License

Add the appropriate project license here.

## Author

**Ahmad Raza**

**SnapClass** — AI-powered classroom attendance management system.
