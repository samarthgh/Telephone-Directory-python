# Telephone Directory

This project is a telephone directory implemented using the Tkinter library in Python with a SQL backend. It allows users to add, search, and delete contacts based on their name, address, and phone number.

## Installation

To use this project, please follow the instructions below:

1. Make sure you have Python installed on your system.
2. Download the provided `contacts.db` database file and store it in the same directory as the Python code.
3. Install the required dependencies by running the following command:

   ```
   pip install tkinter
   ```

## Usage

1. Run the Python script to launch the telephone directory application.
2. The main window will appear with a title "Telephone Directory" and a form to add new contacts.
3. Enter the contact details (first name, last name, address, and phone number) in the respective input fields.
4. Click the "Add Contact to Directory" button to save the contact to the directory.
5. To search for a contact, enter the contact's ID in the search field in the second frame and click the "Search" button.
6. The contact's details will be displayed in the third frame.
7. To edit a contact, click the "Edit" button next to the contact's details in the third frame.
8. A new window will open with the contact's details populated in the input fields.
9. Modify the contact's details as needed and click the "Save Changes" button to update the contact.
10. To delete a contact, enter the contact's ID in the search field and click the "Delete" button.
11. A confirmation dialog will appear to confirm the deletion.
12. Click "Yes" to delete the contact or "No" to cancel the deletion.
13. The contact list can be displayed in the fourth frame by clicking the "Show All Contacts" button.

## Database Schema

The application uses an SQLite database with a single table named "records." The table schema is as follows:

```
CREATE TABLE records (
    first_name TEXT,
    last_name TEXT,
    address TEXT,
    phone_number INTEGER
)
```

The columns in the table correspond to the contact's first name, last name, address, and phone number.

## Note

The code snippet provided includes the creation of the database table. If you already have the `contacts.db` file with the table created, you can comment out or remove the code related to table creation:

```python
# connector = sqlite3.connect('contacts.db')
# cur = connector.cursor()
# cur.execute("""CREATE TABLE records (
#     first_name text,
#     last_name text,
#     address text,
#     phone_number integer
# )""")
# connector.commit()
# connector.close()
```

You can run the script without the table creation code if the database file and table already exist.
