# Medical-Management-System (C++ File-Based)

This is a **console-based Medical Management System** written in **C++**, which uses **text files** for persistent storage.  
The program allows users to manage medicine and patient-related data such as adding, viewing, modifying, and deleting records.

---

##  Features

- Add new medicine and patient details
- Remove existing medicine records
- Modify existing medicine records
- Display details of a single medicine
- Display all stored medicine records
- List all medicine IDs
- File-based data storage (no database required)

---


Each medicine record occupies **8 lines** followed by a blank line.

---

##  Data Stored Per Record

- Medicine ID
- Patient Name
- Patient Age
- Disease
- Supplier ID
- Medicine Price
- Medicine Quantity
- Total Price

## Menu Options

- Add Medicine Data
-	Remove Medicine Data
-	Modify Medicine Data
-	Display One Medicine Record
-	Display All Medicine Records
-	List All Medicine IDs
-	Exit Program

 
 ## Notes

- Medicine ID must be unique

- Records are handled sequentially (no indexing)

- Deletion and modification use a temporary file approach

- Designed for learning file handling and OOP concepts


## How the Program Works Internally
## Class: hospital

- The hospital class:

- Stores all patient and medicine fields

- Contains all business logic

- Handles file reading and writing

- It acts as:

- Data model

- Controller

- Service layer

## Adding Medicine Data

- Flow:

- User enters a Medicine ID

- Program checks if it already exists (check_exist)

- If unique:

- User enters patient & medicine details

- Total price is calculated

- Data is appended to data.txt

## Checking Existing Records

- The function:

- bool check_exist(string id)


- Reads file line-by-line

- Searches for "Medicine id : <id>"

- Prevents duplicate entries

## Display One Medicine Record

- Searches for matching Medicine ID

- Prints the next n lines (8 lines)

- If not found, shows "No data found"

- This works because each record has fixed length.

##  Display All Medicine Records

- Reads entire data.txt

- Prints everything line-by-line

- No filtering applied

## List All Medicine IDs

- Scans the file

- Prints only lines starting with:

- Medicine id :


## Useful for quick lookup.

- Removing Medicine Data (Important Logic)

- Since files cannot delete lines directly:

- Read data.txt

- Copy all lines except the target record to temp.txt

- Rewrite data.txt from temp.txt

- This is called the Temporary File Replacement Technique.

## Modifying Medicine Data

- Modification is done as:

- Remove the old record

- Take new input

- Write updated record back

- This ensures:

- Data integrity

- No partial updates

- Safe file operations

![image](https://github.com/demoslayer/Medical-Management-System/assets/107707267/eb3f01fa-fc6d-4e27-b8e9-8dc67fc697d6)
![image](https://github.com/demoslayer/Medical-Management-System/assets/107707267/948fcd8c-2168-4bd6-9fbb-f6a15b256a1c)
![image](https://github.com/demoslayer/Medical-Management-System/assets/107707267/4a8586a9-c732-40e4-b5c7-c119076ad801)
![image](https://github.com/demoslayer/Medical-Management-System/assets/107707267/84420f92-1d9c-41f3-9508-3162d036da87)
![image](https://github.com/demoslayer/Medical-Management-System/assets/107707267/93524fce-aaf5-4d3d-ab1b-ee64e30e453c)
![image](https://github.com/demoslayer/Medical-Management-System/assets/107707267/392a2e2b-78fb-4061-bc25-0910dace7715)
![image](https://github.com/demoslayer/Medical-Management-System/assets/107707267/10b1c637-827a-47d3-9a0b-9faed52975a5)
![image](https://github.com/demoslayer/Medical-Management-System/assets/107707267/895f8ccf-6543-4824-b4fd-c9cf623c5dc0)
![image](https://github.com/demoslayer/Medical-Management-System/assets/107707267/6d2abae2-5946-4cc4-9335-d1c4d4bac602)
