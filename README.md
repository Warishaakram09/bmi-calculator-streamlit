# 💪 BMI Calculator - Streamlit App

This is a simple **BMI (Body Mass Index)** Calculator built using **Python** and **Streamlit**.  
Users can input their **height** and **weight**, and the app will calculate their BMI and show a health category.

---

## 🚀 How to Run

### Step 1: Install Dependencies

```bash
pip install streamlit
Step 2: Save this code in a file named app.py
python
Copy
Edit
import streamlit as st

st.title("💪 Simple BMI Calculator")

height = st.number_input("Enter your height (in meters)", min_value=0.0, format="%.2f")
weight = st.number_input("Enter your weight (in kilograms)", min_value=0.0, format="%.2f")

if st.button("Calculate BMI"):
    if height > 0 and weight > 0:
        bmi = weight / (height ** 2)
        st.success(f"Your BMI is: {bmi:.2f}")

        if bmi < 18.5:
            st.info("You are Underweight.")
        elif 18.5 <= bmi < 25:
            st.success("You are Normal weight.")
        elif 25 <= bmi < 30:
            st.warning("You are Overweight.")
        else:
            st.error("You are Obese.")
    else:
        st.error("Please enter valid height and weight.")
Step 3: Run the App
bash
Copy
Edit
streamlit run app.py
Then open the link shown in your terminal (usually http://localhost:8501) to use the app.

📊 What is BMI?
BMI (Body Mass Index) is a number calculated using a person's height and weight.
It is used to indicate whether a person is underweight, normal weight, overweight, or obese.

📌 BMI Categories
Underweight: BMI < 18.5

Normal weight: 18.5 ≤ BMI < 25

Overweight: 25 ≤ BMI < 30

Obese: BMI ≥ 30

👩‍💻 Built With
Python

Streamlit

✍️ Author
Warisha Akram

yaml
Copy
Edit
