# Scraping FCSE

This project aims to automate the scraping of various resources from the FCSE (Faculty of Computer Science and Engineering) website. The primary goal is to extract and store relevant academic information in a structured database. The current feature focuses on grading subjects, with more features planned for future development.

## Project Structure

- **scraping_fcse/**: Project directory containing the core Python scripts for grading of the subjects from all programs in fcse.
  - `program_2018.py`: Script to handle the extraction and processing of data from the 2018 program PDFs.
  - `program_2023.py`: Script to handle the extraction and processing of data from the 2023 program PDFs.
  - `script.py`: The main script that orchestrates the downloading, parsing, and storage of grading information from the PDFs. Running this script will populate the `data` folder with a SQLite database (`subjects.db`) containing the extracted information.

- **data/**: Directory where the SQLite databases are stored.
  - `subjects.db`: SQLite database that holds the extracted grading information. This file is automatically generated when running `script.py`.

- **pdf_tmp/**: Temporary storage for downloaded PDFs. These files are processed and then saved here. This directory is automatically filled with PDFs when running `script.py`
- **requirements.txt**: 

## How to Run

1. **Ensure Python Environment**:
   - Make sure you have Python installed on your machine.
   - Install the required dependencies by running:
     ```bash
     pip install -r requirements.txt
     ```

2. **Running the Script**:
   - Navigate to the desired directory and run the following command:
     ```bash
     python script.py
     ```
   - This script will automatically:
     - Scrape the necessary links from the FCSE website.
     - Download the relevant PDFs to the `pdf_tmp/` folder.
     - Extract selected information and store it in the `*.db` SQLite database located in the `data/` folder.

## Future Development

This project is just beginning, and the grading feature is one of many planned. Future features and enhancements include:

- **Expanding Scraping**: Implementing additional scripts to scrape more types of data from the FCSE website.
- **Data Analysis**: Adding tools to analyze the stored data, providing insights into various academic trends.
- **Automation**: Setting up scheduled tasks to automatically update the database with new information.

Stay tuned for more updates!

## License

This project is licensed under the MIT License.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request with your changes.
