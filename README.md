 Healthcare Appointment No-Show Prediction Project



 Project Title:

**Healthcare Appointment No-Show Analysis & Prediction**


 Objective:

Predict whether patients will miss their medical appointments and uncover key trends (e.g., SMS reminders, age group, waiting days) to help healthcare providers optimize scheduling and improve attendance.



 Tools & Technologies:

* **Python**: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
* **Power BI**: KPI Cards, Bar/Column Charts, Line Charts, Slicers
* **Jupyter/Colab**: For EDA, data cleaning, and model training


 Dataset:

* Source: Medical Appointment No-Shows Dataset
* Records: \~110,000 patient appointment entries
* Key columns: `ScheduledDay`, `AppointmentDay`, `No_show`, `Age`, `Gender`, `SMS_received`, `Hypertension`, `Diabetes`, etc.



 Data Cleaning Steps (Python):

1. Converted `ScheduledDay` and `AppointmentDay` to datetime.
2. Renamed columns for consistency (e.g., `No-show` → `No_show`).
3. Dropped irrelevant columns: `PatientId`, `AppointmentID`.
4. Removed duplicates and verified missing values.
5. Filtered out invalid data (e.g., negative ages).


 Feature Engineering:

* `WaitingDays` = Difference between scheduled and actual appointment days
* `DayOfWeek` = Weekday of the appointment
* `AgeGroup` = Categorized as Children, Adults, Seniors
* Converted binary fields: `SMS_received`, `No_show`, etc.



 Power BI Dashboard Components:

 KPIs:

* Total Appointments
* No-Show Rate (%)
* Appointments with SMS Reminders
* Total No-Shows

 Charts:

* **No-Show Rate by Age Group** (Bar Chart)
* **No-Show % by Waiting Days** (Line or Scatter Plot)
* **No-Show Rate by Day of Week** (Column Chart)
* **Effect of SMS Received** (Stacked Column)
* **Optional**: City-wise No-Show Rate (if available)

 Filters/Slicers:

* Gender
* Age Bucket
* SMS Received
* Day of Week



 Key Insights:

* Patients who received SMS reminders were more likely to attend.
* Children and seniors had higher no-show rates.
* Longer waiting days between scheduling and appointment increased no-shows.
* Mondays and Fridays showed higher no-show trends.



### 💾 Files Included:

* `cleaned_appointments.csv`: Final dataset with engineered features
* `appointemnt_prediction`: Python notebook with model training
* `appointment_compliance.pbix`: Power BI report file
* `README.md`: This documentation



