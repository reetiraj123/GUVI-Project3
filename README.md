# GUVI-Project3
PROJECT 3` FOR GUVI HCL for internship under full stack web development TOPIC: QUIZ APPLICATION

Introduction
This project provides an "exam" app that lets users take an online programming quiz.

Features
Define fairly complicated programming problems and have users solve the problem.
Immediate verification of code solution.
Supports pretty much arbitrary coding questions in Python, C, C++, Java, R, Scilab and Bash.
Supports Multiple choice, Fill in the blanks, Arrange options and File upload based questions.
Since it runs on Python, you could technically test any Python based library.
Create course with lessons and quiz for online learning.
Almost real-time monitoring for quiz.
Supports automatic and manual grading, regrading of quiz.
Add grading system to the course.
Scales to over 500+ simultaneous users.
https://github.com/codespaces/new/reetiraj123/GUVI_Project3?auto_init=1&resume=1
https://github.com/reetiraj123/GUVI_Project2
nstallation
Note: Currently, only Linux and MacOS is supported for the project.

If Python 3.6 and above is not available in the system, then we recommend using miniconda. Download miniconda with Python 3.6 and above.

Installing Miniconda

Download miniconda from https://docs.conda.io/en/latest/miniconda.html according to the OS version.
Follow the installation instructions as given in https://conda.io/projects/conda/en/latest/user-guide/install/index.html#regular-installation
Restart the Terminal.
Pre-Requisite

Install redis server

Redis is required for celery. Celery runs a background task to re-evaluate the submissions.

sudo apt install redis-server (Debian/Ubuntu)

yum install redis (Centos)
Start redis server

systemctl start redis
Check redis server status

systemctl status redis
Run celery worker

celery -A online_test worker -B
Ensure pip is installed

Installing Yaksh

Clone the repository

git clone https://github.com/FOSSEE/online_test.git
Go to the online_test directory

cd online_test
Install the dependencies:

Install Django and dependencies

pip3 install -r requirements/requirements-common.txt
Install Code Server dependencies

sudo pip3 install -r requirements/requirements-codeserver.txt
Quick Start
Start up the code server that executes the user code safely:

To run the code server in a sandboxed docker environment, run the command:

$ invoke start
Make sure that you have Docker installed on your system beforehand. Docker Installation

To run the code server without docker, locally use:

$ invoke start --unsafe
Note this command will run the yaksh code server locally on your machine and is susceptible to malicious code. You will have to install the code server requirements in sudo mode.

On another terminal, run the application using the following command:

$ invoke serve
Note: The serve command will run the django application server on the 8000 port and hence this port will be unavailable to other processes.
Open your browser and open the URL http://localhost:8000/exam

Login as a teacher to edit the quiz or as a student to take the quiz Credentials:

Student - Username: student | Password: student
Teacher - Username: teacher | Password: teacher
User can also login to the Default Django admin using;

Admin - Username: admin | Password: admin
