# 💡 Performance Testing Project using Apache JMeter

This project uses **Apache JMeter** to simulate and test both **Web UI interactions** and **RESTful API performance**. The goal is to evaluate system behavior under controlled virtual users, focusing on response times and reliability.

---

## ⚙️ Tools & Tech Stack

- **Apache JMeter 5.5**
- CSV Data Set Config
- HTTP Request & Header Manager
- Regular Expression Extractor
- Assertions (Status/Response Time)
- Aggregate Report, View Results Tree

---

## 🌐 Target Applications

- **UI Testing:** [Pet Store](https://petstore.octoperf.com/actions/Catalog.action)
- **API Testing:** [Restful Booker](https://restful-booker.herokuapp.com/)

---

## 🧪 Test Scenarios

### 🔹 Web UI Testing – PetStore

Simulates end-user flow on a sample e-commerce website:
- **Homepage load**
- **User login** – SignIn request  
- **User registration** – Register1 request  
- **Product search & interaction**:
  - View product (Fish)
  - Add to cart
  - Update quantity
  - Checkout process

### 🔹 API Testing – Restful Booker

Validates key REST API operations for booking management:
- Create auth token
- Create a new booking
- Fetch all booking IDs
- Update booking by ID
- Delete booking by ID

Includes usage of:
- **HTTP Header Manager**
- **Regular Expression Extractor** (to extract tokens/IDs)
- **Assertions** for verifying status codes and response data

---

## 🚦 Load Configuration

### Thread Group: API
- **Users (Threads):** 1  
- **Ramp-up Time:** 1 sec  
- **Loop Count:** 1  
- **Duration:** 600 seconds (set for lifetime if needed)

> 🧪 Ideal for functional and low-load testing. For stress/load testing, increase threads and iterations.

---

## ▶️ Running the Test

### 🖥 GUI Mode
1. Open JMeter
2. Load `JMeter_Assignment.jmx`
3. Click **Start**
4. Monitor:
   - **View Results Tree**
   - **Aggregate Report**

### 💻 Non-GUI Mode (Recommended)
```bash
jmeter -n -t JMeter_Assignment.jmx -l results.jtl -e -o report/
