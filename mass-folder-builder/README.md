# Mass Folder Builder

[![English](https://img.shields.io/badge/lang-English-blue)](README.md)  
[![Bahasa Indonesia](https://img.shields.io/badge/lang-Indonesia-red)](README.id.md)

The **Mass Folder Builder** project contains a Python script to automatically create multiple subfolders within a specified main folder. This is useful for quickly generating large sets of folders for organizing files or testing purposes.

## Features

- Creates a specified number of subfolders with customizable names.
- Allows customization of the main folder path.
- Supports adding a prefix to folder names for better organization.
- Provides clear feedback in the terminal using status tags:
  - `[Info]` for general information.
  - `[Success]` for successfully created folders.
  - `[Skip]` for folders that already exist.
  - `[Error]` for invalid input or issues.
- Prevents the terminal from closing immediately after execution, allowing users to review the output.

## Requirements

- Python 3.x installed on your system.

## Usage

### Step 1: Clone the Repository

To begin, clone this repository to your local machine using the sparse checkout method to get only the necessary project files.

```bash
git clone --no-checkout https://github.com/bektidk/ffos.git
cd ffos
git sparse-checkout init --cone
git checkout main
git sparse-checkout set mass-folder-builder
cd mass-folder-builder
```

### Step 2: Run the Script

In your terminal or command prompt, navigate to the project directory and run the script:

```bash
python create_folders.py
```

### Step 3: Input Details

The script will prompt you for the following inputs:

- Main Folder Path: Specify the directory where subfolders should be created.
- Folder Prefix: Optionally, add a prefix to folder names (e.g., "Folder "). Leave blank for no prefix.
- Number of Folders: Enter the number of folders to create.

### Step 4: Check the Result

After the script completes, you will find subfolders created in the specified main folder. The folder names will be sequential and prefixed if specified. The terminal will remain open, allowing you to review the results.

## Example

Here is an example session:

```bash
----------------------------------------
Welcome to Mass Folder Builder!
----------------------------------------
Enter the main folder path: G:/My Projects
Enter a prefix for the folders (leave blank for none): Folder
Enter the number of folders to create: 5
----------------------------------------
Creating 5 folders in: G:/My Projects
----------------------------------------

[Info] Main folder already exists at: G:/My Projects
[Success] Folder 'Folder 1' created.
[Success] Folder 'Folder 2' created.
[Success] Folder 'Folder 3' created.
[Success] Folder 'Folder 4' created.
[Success] Folder 'Folder 5' created.

----------------------------------------
Process completed! Check your folders.
----------------------------------------

Press Enter to exit...
```

## Notes

- Ensure that the specified directory exists before running the script, as the script will not create the main folder if it does not already exist.
- If a folder already exists, the script will notify you and skip its creation.
- Use meaningful prefixes to better organize your folders.
- The script will wait for you to press Enter before closing the terminal.
