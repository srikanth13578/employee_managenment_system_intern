# Employee Management System 👥

Developed during my internship, this is a full-stack Java application designed to manage corporate employee records efficiently. It uses Server-Side Rendering (SSR) to deliver a fast and secure administrative experience.

🚀 **Live App URL:** [Click Here to View Application](https://https://employeemanagenmentsystemintern-production.up.railway.app/showNewEmployeeForm)

---

## 🛠 Tech Stack
- **Backend:** Java, Spring Boot
- **Frontend:** Thymeleaf, HTML5, CSS3, Bootstrap
- **Database:** MySQL
- **Tools:** Spring Data JPA, Hibernate, Maven

## ✨ Key Features
- **Full CRUD Operations:** Add, update, view, and delete employee profiles.
- **Dynamic Rendering:** Used Thymeleaf to bind backend data directly to the UI.
- **Relational Database:** Organized employee data with MySQL.
- **Responsive Design:** Styled with Bootstrap for a clean look on all devices.

## 📸 Screenshots
Home Page
<img width="1366" height="646" alt="EMP Home Page" src="https://github.com/user-attachments/assets/d0917e10-7451-4311-ba51-4ff8f16c6334" />

Employee-List-Dashboard
<img width="1366" height="642" alt="EMP list and CRUD op" src="https://github.com/user-attachments/assets/7e969e22-3645-4066-b7de-f0cafd620e0f" />


## ⚙️ Installation & Setup

### Method A: 🐳 The Dockerized Setup (Recommended & Quickest)
This project is fully containerized and orchestrated using **Docker** and **Docker Compose**. It completely wraps the Java runtime environment and pairs it with a dedicated, isolated MySQL container instance to enable total environment predictability with zero host dependency installations.

#### Architecture Breakdown
* **Application Layer Container (`employee-management-app`):** Leverages a multi-stage Docker compilation script. Stage 1 triggers a native Maven package wrapper tool directly inside an isolated environment to generate clean binary `.jar` targets. Stage 2 executes the payload cleanly on a lightweight **Eclipse Temurin OpenJDK 17** machine image on container port `1031`.
* **Data Layer Container (`employee-db`):** Spins up an explicit MySQL 8.0 engine running internally on virtual bridge networks while mapping database communication externally to your laptop via port `3309` to bypass native machine database port blocks.

#### 🚀 Execution Steps
1. Navigate to the root directory containing your `docker-compose.yml` file and trigger the build process:
   ```bash
   docker compose up --build
   ```
   *Note: For subsequent runs, you can drop the `--build` flag to launch the entire system instantly in under 3 seconds:*
   ```bash
   docker compose up
   ```
2. **Access the Application:** Open your web browser and go to your live local dashboard:
   ```text
   http://localhost:8082
   ```

---

### Method B: Manual Local Setup (Traditional Approach)

#### 1. Database Configuration
1. Create a MySQL database named `demo`.
2. Open `src/main/resources/application.properties` and update your MySQL `username` and `password`.

#### 2. Run the Application
```bash
# Run using Maven
mvn clean package
mvn spring-boot:run
```

#### 3. Access the App
Once the console stabilizes, open your browser to:
```text
http://localhost:8082

```
🎓 Internship Learnings
- Gained hands-on experience with the **Spring Ecosystem** in a professional setting.
- Learned how to manage **Data Persistence** using JPA and MySQL.
- Optimized server-side rendering for better application performance.
