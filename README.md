# 🚚 Route Creator Form – Customer Service Guide

Welcome! This guide will walk you through how to correctly use the **Route Creator Form** to retrieve and validate route data before creating a route in Samsara.

---

## 🧠 What This Form Does

This form:
- Builds a **standardized route name**
- Links the route to a **warehouse and truck**
- Sends the data to our system (n8n)
- Returns **route stops and validation data**
- Allows you to **verify everything before final creation**

---

## ⚠️ Critical Rule

> ✅ The **first and last stop MUST match the selected warehouse**

Always verify this before proceeding.

---

## 🪜 Step-by-Step Instructions

### 1. Build the Route Name

Use the **Route Name Builder**:

- **City** → Select the correct service region  
- **Month** → Choose the route month  
- **Year** → Defaults to current year (adjust if needed)  
- **Route #** → Choose route number (1–3)

📌 The system will automatically generate a name like:

ROUTES EXAMPLE : New York Apr 2026 Route 3


---

### 2. Confirm Route Name Preview

- Check the **Generated Route Name**
- Make sure it follows the correct format and matches the request

🚫 Do NOT continue if this is incorrect

---

### 3. Select Warehouse

Choose the correct warehouse:
- Texas Warehouse
- Florida Warehouse

⚠️ This must match:
- Route origin
- First & last stop

---

### 4. Select Truck

Choose the assigned vehicle:
- Example: `2020 / Freightliner 006`, `Box Truck 3 / Isuzu 2021`, etc.

📌 Make sure this matches dispatch planning

---

### 5. Set Planned Departure

- **Date** → Required  
- **Time** → Required  

The system converts this into a precise timestamp for routing.

---

### 6. Submit the Form

Click: Retrieve Route Data


This sends the request to the system and retrieves route details.

---

## 🔍 After Submission (VERY IMPORTANT)

### 1. Check Status Message

- ✅ Success → Data retrieved  
- ❌ Error → Fix missing/incorrect fields

---

### 2. Review Validation Panel

This shows:
- Your submitted data
- Full system response

📌 Use this to confirm:
- Route name is correct
- All fields were properly sent

---

### 3. Review Retrieved Stops

Each stop will display:
- Address
- Arrival time
- Departure time
- Coordinates

---

## ✅ What to Verify Before Proceeding

Before creating the route in Samsara, confirm:

- ✔ Route name is correct  
- ✔ Warehouse is correct  
- ✔ Truck is correct  
- ✔ Departure date/time is correct  
- ✔ Stops are returned  
- ✔ First stop = Warehouse  
- ✔ Last stop = Warehouse  

---

## 🔁 Resetting the Form

Click: Reset Form


This will:
- Clear all fields
- Reset route preview
- Clear results and stops

---

## ❌ Common Mistakes

### Missing Route Name
- All 4 fields must be selected:
  - City, Month, Year, Route #

---

### Missing Warehouse or Truck
- The system will block submission

---

### Missing Date or Time
- Both are required to generate the route timestamp

---

### No Stops Returned
- Check the **Validation Panel**
- The data may still exist but not in expected format
- Escalate if needed

---

### Incorrect Warehouse in Stops
🚨 DO NOT proceed  
- Route must start and end at the selected warehouse

---

## 🧩 What Happens Behind the Scenes

When you submit:
- Data is sent to our **n8n webhook**
- System processes route logic
- Returns structured route + stops
- Stops are automatically extracted and displayed

---

## 🏁 Final Step

Once everything is verified:

👉 Proceed to create the route in **Samsara**

---

## 💬 Need Help?

If something looks wrong:
- Take a screenshot of:
  - Validation Panel
  - Stops section
- Escalate with route name + issue

---

**Accuracy here prevents routing errors, delays, and failed deliveries.**