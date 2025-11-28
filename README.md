# ITCorpTimeAnalytics 🕒

**Corporate web platform for time tracking and management analytics in
an IT company**

> Time Tracking • Business Analytics • Workforce Management • Spring
> Boot • Java • MySQL • Dashboard • KPI

## 1. 📋 About the Project

### 1.1. Purpose

**ITCorpTimeAnalytics** is a demonstration corporate web system for:

-   employee time tracking\
-   project and task management\
-   financial accounting\
-   management analytics and reporting

### 1.2. Key Features

-   Analytics for projects, employees, and teams\
-   Performance calculation for periods: day, week, month, quarter,
    year\
-   Financial control of income and expenses\
-   KPI, charts, diagrams, dashboards\
-   Ready-to-extend architecture for custom client technical
    requirements

### 1.3. Target Audience

-   Executives\
-   Project managers\
-   HR specialists\
-   Top management\
-   Investors and corporate solution customers

### 1.4. Important Limitations

-   The application operates **exclusively in demo mode**\
-   Not intended for production use\
-   Represents a **basic implementation** with the ability to be extended for customer requirements

## 2. 📊 Core System Entities

### 2.1. Input Data (Tables)

-   **👥 Employee Management** - full name, position, role, pay rate\
-   **🚀 Project Management** - name, customer, planned/actual dates,
    budget\
-   **✅ Task Management** - description, assignee, planned/actual
    time\
-   **⏱️ Time Tracking** - employee, date, hours, project, category\
-   **💰 Financial Accounting** - project income/expenses

### 2.2. Output Data (Charts, Diagrams, Progress Bars, KPI Metrics, Tables, Printable Reports)

-   **📊 Analytics Dashboards** - tracking aggregated analytical
    indicators\
-   **📈 Advanced Analytics** - tracking detailed reporting indicators
    with print export capability

### 2.3. Period Filtering

-   All reports and analytics support filtering by: day, week, month,
    quarter, year\
-   Ability to set a custom date range

## 3. 🏗️ Architecture

### 3.1. Web Application Format

-   Classic MVC application (Spring Boot MVC)

### 3.2. Frontend

-   **Web Interface Architecture**: Hybrid SSR + AJAX\
-   **Rendering**: Main page layout rendering is SSR (server-side). Dynamic content (charts, tables, filtering) is loaded via asynchronous AJAX requests without full page reload.\
-   **Technology Stack**: Thymeleaf, Bootstrap 5, JavaScript (ES6+), Chart.js, DataTables.js, AJAX/Fetch API

#### 3.2.1. Modular Frontend Architecture (Functional JS Modules)

Each `.js` file represents a separate **targeted functional UI module**

    ITCorpTimeAnalitics/web/src/main/resources/static/js/
    ├── app.js     # Main application initialization entry point
    ├── config.js  # Frontend configuration
    ├── utils.js   # Common utilities
    └── modules/
       ├── analytics.js  # Extended performance analytics
       ├── dashboard.js  # Aggregated analytics dashboard
       ├── employees.js  # Employee management
       ├── filters.js    # Period filter management
       ├── finance.js    # Financial module
       ├── modals.js     # Modal window management
       ├── projects.js   # Project management
       ├── tasks.js      # Task management
       └── timesheets.js # Time tracking

### 3.3. Backend

-   **Architecture**: Modular monolith (multi-module monolith)\
-   **Framework**: Spring Boot 3.2.0\
-   **Database**: MySQL + Hibernate\
-   **Security**: Spring Security\
-   **Technology Stack**: Java 20, Spring Boot 3.2.0, Spring MVC (web layer), Spring Data JPA (data access), Maven (build and dependencies)

#### 3.3.1. Backend Modular Architecture

    ITCorpTimeAnalitics/
    ├── app/                   # Main startup module
    ├── common/                # Shared DTOs and utilities
    ├── persistence/           # Database entities and repositories
    ├── service/               # Business logic
    ├── web/                   # Controllers and views
    ├── security/              # Security configuration
    └── parent pom.xml

## 4. 🚀 Launch and Deployment

### 4.1. Prerequisites

-   Java 20\
-   MySQL 8.0+

### 4.2. Running the Project via Demo JAR File

#### 4.2.1. Create the Database

``` sql
CREATE DATABASE it_corp_time_analitics;
```

#### 4.2.2. Download the executable `app-0.0.1-SNAPSHOT.jar` using the provided link and place it in any folder

👉 [**Download app-0.0.1-SNAPSHOT.jar**](https://github.com/NovakEvgeniy/ITCorpTimeAnalitics/releases/download/v2.0.0/app-0.0.1-SNAPSHOT.jar)

#### 4.2.3. Create the `application.properties` file and place it in the same folder as `app-0.0.1-SNAPSHOT.jar`

``` bash
spring.datasource.url=jdbc:mysql://localhost:3306/it_corp_time_analitics
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

#### 4.2.4. Run the executable file in the folder containing `application.properties` and `app-0.0.1-SNAPSHOT.jar`

``` bash
java -jar app-0.0.1-SNAPSHOT.jar
```

#### 4.2.5. Additional Information

-   Maven installation is not required\
-   Running the JAR file does not provide access to the source code

### 4.3. Launch in the Browser

-   **URL: http://localhost:8080/login**

> ⚠️ **WARNING:** The application is distributed in **demo mode**.\
> A test account is used for access:
>
> **Login:** `demo`\
> **Password:** `demo`
>
> These credentials are intended for demonstration purposes only.

## 5. 📈 Future Development

-   Custom modules according to client technical requirements\
-   Advanced BI analytics\
-   Integrations with 1C, ERP, CRM\
-   Export of reports to Excel / PDF

## 6. ⚖️ Licensing

-   This software is proprietary.\
-   The source code is closed and represents the intellectual property of the author.

## 7. 💼 Commercial Use

-   Source code and extended project versions are provided by agreement.

## 8. 📞 Contacts

-   **Email:** **novakevgeniy1953@gmail.com**\
-   **GitHub:** **https://github.com/NovakEvgeniy?tab=repositories**

