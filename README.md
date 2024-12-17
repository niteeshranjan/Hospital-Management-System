# Hospital-Management-System

## Overview

This Hospital Management System is a web-based application designed to streamline the operations of a hospital. It provides functionalities for users to book appointments, view their profiles and appointments, and for administrators to manage patient histories. The application supports user, doctor, and admin login functionalities and ensures seamless interaction between various stakeholders.

## Features

### User Functionalities:

- **User Registration and Login**
- **Book Appointments**:
  - Select a doctor and specialization dynamically from the database.
  - Choose a date and time for the appointment.
- **View Profile**:
  - Display user details and appointments dynamically from the database.
- **View My Appointments**:
  - Show a list of all appointments booked by the user with details like doctor name, specialization, date, and time.

### Admin Functionalities:

- **Admin Login**:
  - Authenticate using credentials stored in the database.
- **View Patient History**:
  - Display all appointments from the database.
- **Delete Patient History**:
  - Allow admins to delete specific patient records.

### Doctor Functionalities:

- **Doctor Login** (Placeholder for future implementation).

## Technology Stack

- **Frontend**: HTML, CSS (with inline and internal styles for customized designs).
- **Backend**: Java Servlets.
- **Database**: Oracle SQL for managing user, doctor, and appointment data.
- **Server**: Apache Tomcat.

## Database Schema

### Tables:

1. **`userlogin`**:

   - `name` (Primary Key)
   - `password`
   - Other user details.

2. **`doctors`**:

   - `name` (Primary Key)
   - `specialization`.

3. **`appointments`**:

   - `patient_name` (Foreign Key references `userlogin.name`)
   - `doctor_name` (Foreign Key references `doctors.name`)
   - `specialization` (Foreign Key references `doctors.specialization`)
   - `appointment_date`
   - `appointment_time`.

## Installation and Setup

1. Clone this repository to your local machine.
   ```bash
   git clone <repository-url>
   ```
2. Set up Oracle Database and create the required tables using the provided SQL scripts.
3. Configure the database connection in your Java application (update `url`, `dbusername`, and `dbpassword` in the servlets).
4. Deploy the project on Apache Tomcat.
5. Access the application via the browser at `http://localhost:8080/HospitalManagementSystem/`.

## Screenshots

- **Index Page**: Displays options for Admin, Doctor, and User login.
- **Book Appointment Page**: Dynamic dropdowns for doctor and specialization selection.
- **Admin Dashboard**: View and delete patient history.

## Future Enhancements

- Add functionalities for doctors to manage appointments.
- Implement email notifications for appointment confirmation.
- Enhance UI/UX with modern design frameworks like Bootstrap.
- Add security features like password encryption and role-based access control.

## Contributing

Feel free to fork the repository and submit pull requests for new features, bug fixes, or improvements.

## License

This project is open-source and available under the MIT License.

---

Thank you for exploring the Hospital Management System! If you encounter any issues or have suggestions, please open an issue or reach out.

