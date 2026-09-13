# Java CI/CD Pipeline with Jenkins & Maven

A complete, end-to-end Continuous Integration and Continuous Deployment (CI/CD) pipeline built for a Java Maven application. This project demonstrates how to automate code checkout, unit testing, packaging, and deployment using Jenkins and Docker.

---

## 📌 Project Overview

This repository contains a Java application created with the Maven quickstart archetype, structured with automated JUnit test cases, and integrated into Jenkins via a declarative `Jenkinsfile`.

The pipeline automatically handles the application lifecycle whenever changes are committed to the repository, ensuring code reliability, test coverage, and automated deployment preparation.

---

## 🛠️ Tech Stack & Tools

* **Programming Language**: Java (JDK 17)
* **Build Tool**: Apache Maven 3.9
* **Testing Framework**: JUnit
* **CI/CD Server**: Jenkins (Docker Engine)
* **Version Control**: Git & GitHub

---

## 🚀 Pipeline Stages

The declarative pipeline defined in the `Jenkinsfile` runs through four primary stages:
