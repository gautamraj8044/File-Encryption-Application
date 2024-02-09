**File Encryption System**

---

**Overview:**

The File Encryption System is a Java application designed to provide users with a secure way to manage their files by encrypting and hiding them within the application's database. The system allows users to perform various operations such as showing hidden files, hiding new files, and unhiding files.

---

**Features:**

1. **User Authentication:** Users can sign up for an account or log in if they already have one. Upon login, users receive a one-time password (OTP) sent to their registered email address for authentication.

2. **File Management:**
   - **Show Hidden Files:** Users can view a list of hidden files along with their IDs.
   - **Hide New File:** Users can hide a new file by providing its path. The file is encrypted and stored securely in the database.
   - **Unhide File:** Users can unhide a file by selecting its ID from the list of hidden files. The file is decrypted and restored to its original path.

3. **OTP Generation and Email Verification:** The system generates OTPs for user authentication during login and account registration. OTPs are sent to users via email for verification purposes.

---

**Components:**

1. **Main Class (`Main`):** Contains the main method to start the application. It initializes the welcome screen and controls the flow of the program.

2. **Views Package:**
   - **Welcome Class (`Welcome`):** Displays the welcome screen with options for login, signup, and exit. Handles user authentication and navigation to the user view.
   - **UserView Class:** Displays the home screen for authenticated users. Provides options for managing files such as showing hidden files, hiding new files, and unhiding files.

3. **Service Package:**
   - **GenerateOTP Class:** Generates random OTPs for user authentication.
   - **SendOTPService Class:** Sends OTPs to users via email for verification.
   - **UserService Class:** Handles user-related operations such as user registration and checking for existing users.

4. **DAO (Data Access Object) Package:**
   - **DataDAO Class:** Handles database operations related to file management such as retrieving, hiding, and unhiding files.
   - **UserDAO Class:** Handles database operations related to user management such as checking user existence and saving new users.

5. **DB Package:**
   - **MyConnection Class:** Manages database connections and provides methods for establishing and closing connections.

6. **Model Package:**
   - **Data Class:** Represents file objects with attributes like ID, file name, path, and email.
   - **User Class:** Represents user objects with attributes like name and email.

---

**Setup Instructions:**

1. Clone the repository to your local machine.
2. Set up a MySQL database and import the provided SQL schema.
3. Update the database connection details in the `MyConnection` class.
4. Build and run the application using an IDE or command line.

---

**Note:**

- Ensure that the necessary dependencies are installed, such as the MySQL JDBC driver.
- Update email configurations in the `SendOTPService` class to use your SMTP server for sending OTP emails.

---

**Contributors:**

-Gautam Raj

---



---

Feel free to contribute to the project by submitting pull requests or reporting issues. Thank you for using the File Encryption System!
