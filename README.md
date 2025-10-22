# PocketMoney - Personal Expense Tracker 💰

<div align="center">

![PocketMoney Banner](https://img.shields.io/badge/PocketMoney-Expense%20Tracker-667eea?style=for-the-badge&logo=wallet&logoColor=white)

**A modern, feature-rich web application for tracking personal expenses and managing your finances**

[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![Java](https://img.shields.io/badge/Java-ED8B00?style=flat&logo=openjdk&logoColor=white)](https://www.java.com/)
[![JSP](https://img.shields.io/badge/JSP-007396?style=flat&logo=java&logoColor=white)](https://en.wikipedia.org/wiki/Jakarta_Server_Pages)
[![Servlet](https://img.shields.io/badge/Servlet-007396?style=flat&logo=java&logoColor=white)](https://jakarta.ee/specifications/servlet/)
[![Chart.js](https://img.shields.io/badge/Chart.js-FF6384?style=flat&logo=chartdotjs&logoColor=white)](https://www.chartjs.org/)
[![Oracle DB](https://img.shields.io/badge/Oracle-F80000?style=flat&logo=oracle&logoColor=white)](https://www.oracle.com/database/)

[Features](#-features) • [Demo](#-demo) • [Installation](#-installation) • [Usage](#-usage) • [Tech Stack](#-tech-stack) • [Architecture](#-architecture) • [Screenshots](#-screenshots)

</div>

---

## 📋 Overview

PocketMoney is a comprehensive personal finance management application that helps users track their daily expenses, visualize spending patterns, and make informed financial decisions. Built with modern web technologies and featuring an intuitive glassmorphism UI design, backed by a robust Java Servlet architecture.

## ✨ Features

### 🎯 Core Features
- **User Authentication** - Secure sign-up and sign-in system with session management
- **Expense Tracking** - Add, view, and categorize expenses with validation
- **Real-time Dashboard** - Visual overview of spending patterns with live data
- **Category Management** - Organize expenses by categories (Food, Transport, Shopping, etc.)
- **Date-based Filtering** - Filter expenses by date range
- **Search Functionality** - Quick search through expense records

### 📊 Analytics & Reports
- **Interactive Charts** - Doughnut and line charts powered by Chart.js
- **Category Breakdown** - Visual representation of spending by category
- **Monthly Reports** - Comprehensive monthly expense analysis
- **Detailed Reports** - Sortable, filterable transaction history
- **Total Spending Overview** - Quick view of total and daily expenses

### 🎨 UI/UX Features
- **Glassmorphism Design** - Modern, translucent card-based interface
- **Responsive Layout** - Mobile-first design that works on all devices
- **Smooth Animations** - CSS animations for better user experience
- **Icon Integration** - Font Awesome icons throughout
- **Color-coded Categories** - Easy visual identification

## 🖥️ Demo

### Screenshots

> **Note:** Add your screenshots to a `screenshots` folder in your repository

#### Homepage
![Homepage](https://github.com/user-attachments/assets/bf30dd90-d4dd-4c46-9ebb-a7d19bd0bd9f)
*Modern landing page with gradient background and glassmorphism effects*

#### Sign In / Sign Up
![Sign In](https://github.com/user-attachments/assets/fe317db5-593b-4ed7-b413-61d53fba3259)
![Sign Up](https://github.com/user-attachments/assets/d385bb52-1dc7-47cd-b574-4cd4298c9ead)
*Secure authentication with animated form fields*

#### Dashboard
![Dashboard](https://github.com/user-attachments/assets/69225bc8-9861-4fe6-9306-951df9e738e9)
*Comprehensive overview with statistics cards and spending charts*

#### Add Expense
![Add Expense](https://github.com/user-attachments/assets/bbb7ff8b-641d-4aa6-a56a-d7c376e35120)
*Intuitive expense entry form with category selection*

#### Detailed Reports
![Reports](https://github.com/user-attachments/assets/69361aad-4c56-44de-845f-8b370d064ffd
)
*Filterable and sortable transaction history*

#### Monthly Category Report
![Category Report](https://github.com/user-attachments/assets/2fcf0746-136b-4f12-876e-f017b0a38e38
)
*Visual breakdown of spending by category over time*

## 🚀 Tech Stack

### Frontend
- **HTML5** - Semantic markup
- **CSS3** - Modern styling with Flexbox/Grid, animations, and glassmorphism
- **JavaScript (ES6+)** - Client-side interactivity and form validation
- **Chart.js v4.x** - Data visualization library
- **Font Awesome 6.4.0** - Icon library
- **Google Fonts (Poppins)** - Typography

### Backend
- **Java 8+** - Core programming language
- **Jakarta Servlets 5.0** - HTTP request handling
- **Java Server Pages (JSP)** - Server-side rendering
- **JDBC** - Database connectivity and operations

### Database
- **Oracle Database 11g/12c** - Data persistence
- Custom schema for user authentication and expense tracking

### Architecture
- **MVC Pattern** - Model-View-Controller architecture
- **DAO Pattern** - Data Access Object for database operations
- **Session Management** - HttpSession for user state
- **Prepared Statements** - SQL injection prevention

## 🏗️ Architecture

### Project Structure
```
pocketmoney/
├── src/
│   └── Money/
│       ├── DBCon.java              # Database connection utility
│       ├── DBTransaction.java      # Database operations (DAO)
│       ├── RegData.java            # User data model (POJO)
│       └── PocketServlet.java      # Main servlet controller
├── WebContent/
│   ├── WEB-INF/
│   │   ├── web.xml                 # Deployment descriptor
│   │   └── lib/
│   │       └── ojdbc8.jar          # Oracle JDBC driver
│   ├── homepage.html               # Landing page
│   ├── signin.html                 # Sign in page
│   ├── signup.html                 # Sign up page
│   ├── dashboard.jsp               # Main dashboard
│   ├── addExpenses.jsp             # Add expense form
│   ├── report.jsp                  # Detailed transaction report
│   ├── monthcat.jsp                # Monthly category report
│   └── logout.jsp                  # Logout handler
└── screenshots/                    # Application screenshots
```

### Class Diagram
```
┌─────────────────┐
│  PocketServlet  │ (Controller)
└────────┬────────┘
         │ uses
         ▼
┌─────────────────┐      ┌──────────────┐
│ DBTransaction   │◄─────┤   RegData    │ (Model)
└────────┬────────┘ uses └──────────────┘
         │ uses
         ▼
┌─────────────────┐
│     DBCon       │ (Utility)
└─────────────────┘
```

### Data Flow
```
User Request → Servlet → DAO → Database
                  ↓
            Session/JSP
                  ↓
            Response (HTML)
```

## 📦 Installation

### Prerequisites
- **Java Development Kit (JDK)** 8 or higher
- **Apache Tomcat** 9.x or higher
- **Oracle Database** 11g or higher
- **IDE** (Eclipse, IntelliJ IDEA, or NetBeans)
- **Web Browser** (Chrome, Firefox, Safari, Edge)

### Database Setup

#### 1. Create Database Schema and Tables
```sql
-- Connect to Oracle as system or your user
-- Create tables for the application

-- Users table
CREATE TABLE pocketusers (
    uname VARCHAR2(50) PRIMARY KEY,
    email VARCHAR2(100) UNIQUE NOT NULL,
    upass VARCHAR2(100) NOT NULL
);

-- Expenses table
CREATE TABLE pexpenses (
    expense_id NUMBER GENERATED ALWAYS AS IDENTITY PRIMARY KEY,
    uname VARCHAR2(50) NOT NULL,
    amount NUMBER(10,2) NOT NULL,
    iname VARCHAR2(100) NOT NULL,
    qty VARCHAR2(50),
    category VARCHAR2(50) NOT NULL,
    pdate DATE NOT NULL,
    CONSTRAINT fk_user FOREIGN KEY (uname) REFERENCES pocketusers(uname)
);

-- Create indexes for better performance
CREATE INDEX idx_uname ON pexpenses(uname);
CREATE INDEX idx_pdate ON pexpenses(pdate);
CREATE INDEX idx_category ON pexpenses(category);
```

#### 2. Insert Sample Data (Optional)
```sql
-- Sample user
INSERT INTO pocketusers VALUES ('demo', 'demo@example.com', 'demo123');

-- Sample expenses
INSERT INTO pexpenses (uname, amount, iname, qty, category, pdate) 
VALUES ('demo', 50.00, 'Lunch', '1', 'Food', SYSDATE);

INSERT INTO pexpenses (uname, amount, iname, qty, category, pdate) 
VALUES ('demo', 30.00, 'Bus Ticket', '1', 'Transport', SYSDATE);

COMMIT;
```

#### 3. Verify Database Connection

Update database credentials in `DBCon.java`:
```java
con = DriverManager.getConnection(
    "jdbc:oracle:thin:@localhost:1521:xe", 
    "system",      // Replace with your DB username
    "0900"         // Replace with your DB password
);
```

### Application Setup

#### Option 1: Using Eclipse IDE

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/pocketmoney.git
```

2. **Import Project**
   - Open Eclipse
   - File → Import → Existing Projects into Workspace
   - Select the cloned repository folder
   - Click Finish

3. **Configure Build Path**
   - Right-click project → Properties → Java Build Path
   - Add Oracle JDBC Driver (`ojdbc8.jar`) to Libraries
   - Add Servlet API JAR if not already included

4. **Configure Tomcat Server**
   - Window → Preferences → Server → Runtime Environments
   - Add Apache Tomcat 9.x
   - Point to your Tomcat installation directory

5. **Deploy and Run**
   - Right-click project → Run As → Run on Server
   - Select Tomcat server
   - Access at `http://localhost:8080/pocketmoney/homepage.html`

#### Option 2: Manual Deployment

1. **Compile Java Classes**
```bash
javac -cp "path/to/servlet-api.jar:path/to/ojdbc8.jar" src/Money/*.java -d build/classes
```

2. **Create WAR File**
```bash
jar -cvf pocketmoney.war -C WebContent/ .
```

3. **Deploy to Tomcat**
   - Copy `pocketmoney.war` to `TOMCAT_HOME/webapps/`
   - Start Tomcat
   - Access at `http://localhost:8080/pocketmoney/homepage.html`

### Dependencies

Add these JARs to `WEB-INF/lib/`:

1. **Oracle JDBC Driver**
   - Download: [Oracle JDBC Downloads](https://www.oracle.com/database/technologies/jdbc-downloads.html)
   - File: `ojdbc8.jar` (for Oracle 12c+)

2. **Servlet API** (provided by Tomcat)
   - `jakarta.servlet-api-5.0.0.jar`

## 📖 Usage

### Getting Started

1. **Create an Account**
   - Navigate to `http://localhost:8080/pocketmoney/homepage.html`
   - Click "Sign Up"
   - Enter username, email, and password
   - Confirm your password
   - Submit the form

2. **Sign In**
   - Click "Sign In" from homepage
   - Enter your credentials
   - You'll be redirected to the dashboard

3. **Add Your First Expense**
   - Click "Add Expense" in the sidebar
   - Fill in the expense details:
     - Amount (numeric)
     - Quantity (e.g., "1kg", "2 items")
     - Item/Service Name
     - Category (dropdown)
     - Purchase Date (date picker)
   - Click "Add Expense"

4. **View Dashboard**
   - See your total spending
   - View today's expenses
   - Check category breakdown with pie chart
   - Review recent transactions

5. **Generate Reports**
   - **Detailed Report**: View all transactions with filtering and sorting
   - **Monthly Category Report**: Analyze spending patterns over time

### API Endpoints

The servlet handles the following operations:
```java
POST /PocketServlet
  - Parameters:
    * b: "Register" | "Sign In"
    * username: String
    * password: String
    * email: String (for registration only)
```

### Session Management
```java
// Session is created on successful login
HttpSession session = request.getSession();
session.setAttribute("un", username);

// Check if user is logged in (in JSP)
String username = (String) session.getAttribute("un");
if (username == null) {
    response.sendRedirect("signin.html");
}
```

## 🗄️ Database Schema

### Table: `pocketusers`

| Column | Type | Constraints |
|--------|------|-------------|
| uname | VARCHAR2(50) | PRIMARY KEY |
| email | VARCHAR2(100) | UNIQUE, NOT NULL |
| upass | VARCHAR2(100) | NOT NULL |

### Table: `pexpenses`

| Column | Type | Constraints |
|--------|------|-------------|
| expense_id | NUMBER | PRIMARY KEY, AUTO-INCREMENT |
| uname | VARCHAR2(50) | FOREIGN KEY → pocketusers(uname) |
| amount | NUMBER(10,2) | NOT NULL |
| iname | VARCHAR2(100) | NOT NULL |
| qty | VARCHAR2(50) | |
| category | VARCHAR2(50) | NOT NULL |
| pdate | DATE | NOT NULL |

### Entity Relationship
```
pocketusers (1) ──────< (many) pexpenses
    uname                    uname (FK)
```

## 💻 Code Structure

### 1. DBCon.java - Database Connection Utility
```java
package Money;
import java.sql.*;

public class DBCon {
    // Returns a database connection
    public static Connection getCon() {
        Connection con = null;
        try {
            Class.forName("oracle.jdbc.driver.OracleDriver");
            con = DriverManager.getConnection(
                "jdbc:oracle:thin:@localhost:1521:xe", 
                "system", 
                "0900"
            );
        } catch(Exception e) {
            System.out.println(e);
        }
        return con;
    }
}
```

**Purpose**: Centralizes database connection logic with singleton pattern.

### 2. RegData.java - User Data Model (POJO)
```java
package Money;

public class RegData {
    private String uname;
    private String email;
    private String upass;
    
    // Getters and Setters
    public String getUname() { return uname; }
    public void setUname(String uname) { this.uname = uname; }
    
    public String getEmail() { return email; }
    public void setEmail(String email) { this.email = email; }
    
    public String getUpass() { return upass; }
    public void setUpass(String upass) { this.upass = upass; }
}
```

**Purpose**: Encapsulates user registration/login data.

### 3. DBTransaction.java - Data Access Object (DAO)
```java
package Money;
import java.sql.*;

public class DBTransaction {
    
    // Insert user registration data
    public int inData(RegData ob) {
        int res = 0;
        try {
            Connection con = DBCon.getCon();
            PreparedStatement ps = con.prepareStatement(
                "INSERT INTO pocketusers VALUES(?,?,?)"
            );
            ps.setString(1, ob.getUname());
            ps.setString(2, ob.getEmail());
            ps.setString(3, ob.getUpass());
            res = ps.executeUpdate();
            con.close();
        } catch(Exception e) {
            System.out.println(e);
        }
        return res;
    }
    
    // Verify user credentials
    public int checkData(RegData ob) {
        int res = 0;
        try {
            Connection con = DBCon.getCon();
            PreparedStatement ps = con.prepareStatement(
                "SELECT uname, upass FROM pocketusers WHERE uname=? AND upass=?"
            );
            ps.setString(1, ob.getUname());
            ps.setString(2, ob.getUpass());
            ResultSet rs = ps.executeQuery();
            if(rs.next()) {
                res = 1;
            }
            con.close();
        } catch(Exception e) {
            System.out.println(e);
        }
        return res;
    }
}
```

**Purpose**: Handles all database operations for user authentication.

### 4. PocketServlet.java - Main Controller
```java
package Money;

import jakarta.servlet.*;
import jakarta.servlet.annotation.WebServlet;
import jakarta.servlet.http.*;
import java.io.IOException;

@WebServlet("/PocketServlet")
public class PocketServlet extends HttpServlet {
    
    protected void doPost(HttpServletRequest request, HttpServletResponse response) 
            throws ServletException, IOException {
        
        String btn = request.getParameter("b");
        PrintWriter out = response.getWriter();
        RegData ob = new RegData();
        
        // Handle Sign In
        if(btn.equals("Sign In")) {
            ob.setUname(request.getParameter("username"));
            ob.setUpass(request.getParameter("password"));
            ob.setEmail("");
            
            if(new DBTransaction().checkData(ob) == 1) {
                HttpSession session = request.getSession();
                session.setAttribute("un", request.getParameter("username"));
                response.sendRedirect("dashboard.jsp");
            } else {
                out.println("Invalid username or password");
            }
        }
        
        // Handle Registration
        if(btn.equals("Register")) {
            ob.setUname(request.getParameter("username"));
            ob.setEmail(request.getParameter("email"));
            ob.setUpass(request.getParameter("password"));
            
            if(new DBTransaction().inData(ob) == 1) {
                response.sendRedirect("signin.html");
            }
        }
    }
}
```

**Purpose**: Central controller handling user authentication requests.

## 🔒 Security Features

### Implemented Security Measures

1. **SQL Injection Prevention**
   - Uses PreparedStatements throughout
   - Parameterized queries for all database operations

2. **Session Management**
   - HttpSession for user state tracking
   - Session validation on protected pages
   - Automatic redirect on unauthorized access

3. **Password Security**
   - Client-side password validation
   - Password confirmation on registration
   - ⚠️ **Note**: Consider adding password hashing (bcrypt/SHA-256) for production

4. **Input Validation**
   - Client-side form validation
   - Server-side data type checking
   - Required field enforcement

### Recommended Security Enhancements
```java
// Add password hashing (example with SHA-256)
import java.security.MessageDigest;

public String hashPassword(String password) {
    try {
        MessageDigest md = MessageDigest.getInstance("SHA-256");
        byte[] hash = md.digest(password.getBytes());
        StringBuilder hexString = new StringBuilder();
        for(byte b : hash) {
            hexString.append(String.format("%02x", b));
        }
        return hexString.toString();
    } catch(Exception e) {
        return null;
    }
}
```

## 🎨 Design Features

### Glassmorphism UI
- Semi-transparent backgrounds with backdrop blur
- Subtle borders and shadows
- Gradient backgrounds
- Modern, clean aesthetic

### Responsive Design
- Mobile-first approach
- Flexible grid layouts
- Touch-friendly interface
- Breakpoints: 480px, 768px, 1024px

### Animations
- Fade-in effects on page load
- Smooth transitions on hover
- Animated background shapes
- Button hover effects with gradients

## 🐛 Troubleshooting

### Common Issues and Solutions

#### 1. Database Connection Error
```
Error: java.sql.SQLException: ORA-12154: TNS:could not resolve the connect identifier
```
**Solution**: 
- Verify Oracle service is running
- Check connection string in `DBCon.java`
- Ensure Oracle listener is active: `lsnrctl status`

#### 2. ClassNotFoundException: oracle.jdbc.driver.OracleDriver
```
Error: java.lang.ClassNotFoundException: oracle.jdbc.driver.OracleDriver
```
**Solution**: 
- Add `ojdbc8.jar` to `WEB-INF/lib/`
- Verify JAR is in project build path

#### 3. HTTP 404 - Servlet Not Found
```
Error: HTTP Status 404 – Not Found
```
**Solution**: 
- Check servlet mapping in `@WebServlet` annotation
- Verify form action URL matches servlet path
- Rebuild and redeploy the application

#### 4. Session Attribute Null
```
Error: NullPointerException when accessing session
```
**Solution**: 
- Ensure user logged in successfully
- Check session timeout settings
- Verify session attribute name matches

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Coding Standards

- Follow Java naming conventions
- Add JavaDoc comments for public methods
- Keep methods focused and single-purpose
- Write clean, readable code
- Add comments for complex logic

## 📝 License

This project is licensed under the MIT License.
```
MIT License

Copyright (c) 2025 Sonu

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

## 👨‍💻 Author

**Sonu**
- GitHub:[SONURAYY0900](https://github.com/SONURAY0900)
- LinkedIn: [sonuray-dev](https://linkedin.com/in//sonuray-dev/)
- Email:raysonu0900@gmail.com

## 🙏 Acknowledgments

- [Chart.js](https://www.chartjs.org/) - Data visualization
- [Font Awesome](https://fontawesome.com/) - Icons
- [Google Fonts](https://fonts.google.com/) - Typography
- [Oracle Database](https://www.oracle.com/database/) - Database system
- [Apache Tomcat](https://tomcat.apache.org/) - Servlet container
- Design inspiration from modern fintech applications

## 📚 Additional Resources

- [Jakarta Servlet Documentation](https://jakarta.ee/specifications/servlet/5.0/)
- [Oracle JDBC Tutorial](https://docs.oracle.com/en/database/oracle/oracle-database/19/jjdbc/)
- [Chart.js Documentation](https://www.chartjs.org/docs/)
- [Java Design Patterns](https://java-design-patterns.com/)

## 📧 Support

For questions or support:
- Open an issue on GitHub
- Email:raysonu0900@gmail.com

---

<div align="center">

**Made with ❤️ by Sonu**

⭐ Star this repository if you find it helpful!

![Visitors](https://visitor-badge.laobi.icu/badge?page_id=yourusername.pocketmoney)

</div>
