# Setting Up Odoo Customization Development Environment

## Prerequisites

- Operating System: Windows/Linux/macOS
- Python 3
- PostgreSQL database
- Git

## Steps

1. **Install Python 3**:
   - Download and install Python 3 from the official website or use a package manager like `apt`, `brew`, or `yum`.
   - Ensure that Python 3 is added to the system PATH.

2. **Install PostgreSQL**:
   - Download and install PostgreSQL database from the official website.
   - During installation, note down the username, password, and database name for Odoo.

3. **Install Git**:
   - Download and install Git from the official website or use a package manager.
   - Git will be used to clone the Odoo source code repository.

4. **Clone Odoo Repository**:
   - Open terminal/command prompt.
   - Navigate to the directory where you want to store Odoo source code.
   - Execute the following command to clone the Odoo repository:
     ```bash
     git clone https://github.com/odoo/odoo.git
     ```

5. **Create Virtual Environment**:
   - Navigate to the directory where Odoo repository is cloned.
   - Create a virtual environment using Python 3:
     ```bash
     python3 -m venv odoo-venv
     ```
   - Activate the virtual environment:
     - On Windows:
       ```bash
       odoo-venv\Scripts\activate
       ```
     - On Linux/macOS:
       ```bash
       source odoo-venv/bin/activate
       ```

6. **Install Odoo Dependencies**:
   - Inside the activated virtual environment, install Odoo dependencies using pip:
     ```bash
     pip install -r requirements.txt
     ```

7. **Configure Odoo**:
   - Create a configuration file for Odoo:
     - Copy the `odoo.conf` file from the Odoo repository to a new location.
     - Modify the configuration file as per your PostgreSQL database settings (database name, username, password, etc.).
     - Optionally, configure other settings such as addons path, log level, etc.

8. **Initialize Odoo Database**:
   - Ensure PostgreSQL server is running.
   - Inside the activated virtual environment, run Odoo's database initialization command:
     ```bash
     ./odoo-bin -c /path/to/your/odoo.conf -d your_database_name --init all
     ```

9. **Run Odoo Server**:
   - Inside the activated virtual environment, run the Odoo server:
     ```bash
     ./odoo-bin -c /path/to/your/odoo.conf
     ```
   - Access Odoo application via web browser using the configured URL (usually http://localhost:8069).

10. **Start Customization Development**:
    - Now you have a running Odoo instance and can start developing customizations.
    - Use your favorite code editor or IDE for coding, debugging, and testing your customizations.
    - Deploy your customizations to the running Odoo server for testing.

11. **Version Control**:
    - Use Git for version control of your customization code.
    - Commit changes regularly and push them to your repository.

## Conclusion

You now have a fully functional development environment set up for Odoo customization from the source code. Start developing and enhancing Odoo according to your project requirements.

