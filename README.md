![Concept 3D Printable Vase](https://github.com/user-attachments/assets/53185591-69ff-462a-9a9a-53d1c345c7c2)

> GUI-based application designed for managing STL (stereolithography) 3D model files.

#

This Python program is a comprehensive GUI-based application designed for managing STL (stereolithography) 3D model files. It provides a dark-themed user interface where users can import, view, delete, and annotate 3D model files. The program stores detailed metadata about each STL file, including its name, file path, size, vertex count, volume, model dimensions, modification date, and user-added notes. The application also supports exporting the database contents to a CSV file, enabling easy sharing or backup of the data.

The program uses an SQLite database to store the details of each STL file. Upon initialization, the program checks if the necessary database tables and columns exist, creating or altering them as needed. This ensures that the application can handle new metadata fields without losing compatibility with older versions of the database. The database operations include inserting new records, fetching existing records for display, deleting selected records, and updating records with user-added notes.

The GUI is built using the Tkinter library and provides several controls for interacting with the STL file records. The title bar features buttons for importing STL files, deleting selected records, exporting data to CSV, and adding notes to records. The main window displays a listbox that shows the details of each STL file, allowing for multiple selections for batch operations. The GUI also includes a footer that displays statistics about the total number of files and their combined size in the database.

When STL files are imported, the program reads various metadata attributes using the Trimesh library, including vertex count, volume, and model dimensions. It also retrieves the file's modification date from the operating system. This data is stored in the SQLite database and displayed in the GUI, providing users with a detailed overview of each file's properties. The ability to handle multiple files at once streamlines the process of managing large collections of 3D models.

One of the standout features of this program is the ability to add custom notes to each STL record. This feature allows users to annotate their 3D models with additional information, which can be useful for project management, collaboration, or personal reference. The program's export functionality ensures that all this detailed data can be easily saved and shared, making it a versatile tool for anyone working with 3D models.

#### 3D Model STL File Database Manager V1.0 Topology Diagram

```
Main Application (Tkinter)
|
+-- Database Setup (SQLite Initialization)
|   |
|   +-- Check and Create/Alter Tables
|   +-- Initialize Database Connection
|
+-- GUI Setup
|   |
|   +-- Title Bar
|   |   |
|   |   +-- Add STL Button
|   |   +-- Delete STL Button
|   |   +-- Export to CSV Button
|   |   +-- Add Note Button
|   |
|   +-- Listbox (Displays STL File Details)
|   |   |
|   |   +-- Fetch Data from Database
|   |   +-- Display Metadata and Notes
|   |
|   +-- Footer (Displays Database Statistics)
|       |
|       +-- Update Total Files Count
|       +-- Update Total Size
|
+-- STL File Handling
|   |
|   +-- Import STL Files (Multiple Selection)
|   |   |
|   |   +-- Extract Metadata (File Size, Vertex Count, Volume, etc.)
|   |   +-- Retrieve File Modification Date
|   |   +-- Store Data in Database
|   |
|   +-- Delete STL Files
|   |   |
|   |   +-- Handle Multiple Selections
|   |   +-- Delete from Database
|   |
|   +-- Add Notes to STL Files
|       |
|       +-- Retrieve Selected File
|       +-- Prompt for User Input (Note)
|       +-- Update Database with Note
|
+-- Export Functionality
    |
    +-- Fetch Data from Database
    +-- Save Data to CSV File
```

#
### Related Links

[3D Printing](https://github.com/sourceduty/3D_Printing)
<br>
[Automated 3D Modelling](https://github.com/sourceduty/Automated_3D_Modelling)
<br>
[3D Model Imaging](https://github.com/sourceduty/3D_Model_Imaging)
<br>
[Cults 3D](https://github.com/sourceduty/Cults_3D)

***
Copyright (C) 2024, Sourceduty - All Rights Reserved.
