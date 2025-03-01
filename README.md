# 🌍 Unit Converter App

![Unit Converter](https://img.shields.io/badge/Python-3.8%2B-blue) ![Streamlit](https://img.shields.io/badge/Streamlit-1.0%2B-red) ![License](https://img.shields.io/badge/License-MIT-green)

🚀 A simple and interactive **Unit Converter App** built with **Streamlit**. Convert Length, Weight, and Time units **instantly** with a clean and user-friendly interface.

---

## ✨ Features
- 📏 **Convert Length:** Kilometers ↔ Miles
- ⚖️ **Convert Weight:** Kilograms ↔ Pounds
- ⏱ **Convert Time:** Seconds, Minutes, Hours, Days
- 🎯 **Real-time Conversion**
- 🖥 **Simple & Interactive UI**

---

## 📸 Preview
![Unit Converter App](https://user-images.githubusercontent.com/your-image-link.png)

---

## 🛠 Installation

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/your-username/unit-converter-app.git
cd unit-converter-app
```

### 2️⃣ Install Dependencies
```bash
pip install streamlit
```

### 3️⃣ Run the App
```bash
streamlit run app.py
```

---

## 📝 Step-by-Step Guide

### 1️⃣ Importing Streamlit
```python
import streamlit as st
```
- **Streamlit** is a Python library used to build interactive web applications.
- `st` is the alias for Streamlit, making it easier to call functions.

### 2️⃣ Setting Up the Title and Description
```python
st.title("🌍Unit Converter App")
st.markdown("### Converts Length, Weight And Time Instantly")
st.write("Welcome! Select a category, enter a value and get the converted result in real-time")
```
- `st.title()` adds the **main heading** of the app.
- `st.markdown()` adds a **subheading**.
- `st.write()` displays **an introductory text**.

### 3️⃣ Choosing a Category
```python
category = st.selectbox("Choose a category", ["Length", "Weight", "Time"])
```
- `st.selectbox()` creates a **dropdown menu** for users to select a conversion category:
  - 📏 Length
  - ⚖️ Weight
  - ⏱ Time

### 4️⃣ Function to Convert Units
```python
def convert_units(category, value, unit):
    if category == "Length":
        if unit == "Kilometers to Miles":
            return value * 0.621371
        elif unit == "Miles to Kilometers":
            return value / 0.621371
        
    elif category == "Weight":
        if unit == "Kilograms to pounds":
            return value * 2.20462
        elif unit == "Pounds to kilograms":
            return value / 2.20462
            
    elif category == "Time":
        if unit == "Seconds to minutes":
            return value / 60
        elif unit == "Minutes to seconds":
            return value * 60
        elif unit == "Minutes to hours":
            return value / 60
        elif unit == "Hours to minutes":
            return value * 60
        elif unit == "Hours to days":
            return value / 24
        elif unit == "Days to hours":
            return value * 24
    
    return 0  # Default return if no conversion is selected
```
- The function **convert_units()** takes three inputs:
  - **category** (Length, Weight, or Time)
  - **value** (number to be converted)
  - **unit** (conversion type)
- It performs the **conversion** based on the selected unit and returns the result.

### 5️⃣ Selecting the Conversion Type Based on Category
```python
if category == "Length":
    unit = st.selectbox("📏 Select Conversion", ["Miles to Kilometers","Kilometers to Miles"])
elif category == "Weight":
    unit = st.selectbox("⚖️ Select Conversion", ["Kilograms to pounds", "Pounds to kilograms"])
elif category == "Time":
    unit = st.selectbox("⏱️ Select Conversion", ["Seconds to minutes", "Minutes to seconds", "Minutes to hours", "Hours to minutes", "Hours to days", "Days to hours"])
```
- Depending on the selected category, another **dropdown** appears to choose the **specific conversion unit**.
- `st.selectbox()` is used again to display different conversion options.

### 6️⃣ Taking User Input
```python
value = st.number_input("Enter the value to convert")
```
- `st.number_input()` allows users to **input a number** for conversion.

### 7️⃣ Performing Conversion When Button is Clicked
```python
if st.button("Convert"):
    result = convert_units(category, value, unit)
    st.success(f"The result is {result:.2f}")
```
- `st.button("Convert")` adds a **button** that triggers the conversion when clicked.
- The `convert_units()` function is called with the user inputs.
- `st.success(f"The result is {result:.2f}")` displays the **final converted value**.

---

## 🎯 Final Output
When you run this **Streamlit app**:

✅ It shows a **title, description, and dropdown** for selecting the conversion category.  
✅ Based on the selected category, another **dropdown** appears for choosing a unit conversion.  
✅ A **number input box** allows users to enter a value.  
✅ When clicking **"Convert"**, the app calculates and displays the **converted result**.

---

## 💡 How to Run This Code?
### 🛠 Install Streamlit if not already installed:
```bash
pip install streamlit
```

### 📂 Save the script as `app.py` and run:
```bash
streamlit run app.py
```
This will open a **browser window** with the **Unit Converter App**. 🚀

---

## 🏆 Contributing
Contributions are **welcome**! Feel free to **fork** this repository and submit a **pull request**. 😊

---

## 📄 License
This project is licensed under the **MIT License**.

---

## 📬 Contact
📧 **Email:** mohsinraza@gmail.com  
🔗 **LinkedIn:** [Mohsin Raza](https://www.linkedin.com/in/mohsin-raza-a514392b6)

Happy Coding! 🚀

