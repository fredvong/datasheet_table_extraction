# Optical Data Sheet Extractor

A Python utility to extract "Constants of Dispersion Formula" from optical product datasheets using PDF parsing.

## Project Goals

This project demonstrates:
1. How to use AI-assisted development (Cursor AI) to solve a specific data extraction task
2. Creating a targeted PDF parser for a specific document format (not a generic table extraction tool)
3. The efficiency of using AI tools to quickly develop solutions for well-defined problems

Note: This is not intended to be a generic PDF table extraction tool. Instead, it shows how AI assistance can help create a focused solution for extracting specific data from a known document format.

## Project Background

This project was developed with the assistance of Cursor AI to solve a specific data extraction challenge: parsing multiple optical product datasheets to extract dispersion formula constants from standardized tables.

## The Challenge

- 100+ pages of optical product datasheets in PDF format
- Each datasheet begins with "Data Sheet" and the optic's name
- Target data is in tables titled "Constants of Dispersion Formula"
- First few pages contain marketing materials (to be skipped)
- Need to extract two columns of numerical data (B1, B2, B3, etc.)

## Development Process with Cursor AI

![Cursor AI Development Process](./screenshot.png)

The screenshot above shows the Cursor AI Composer window where the development took place. In this interface:
- The left panel shows the chat interaction where requirements were discussed
- The code editor displays the Python implementation
- You can see the recommended libraries (pdfplumber, pandas, re) and their purposes
- The conversation shows how Cursor AI helped structure the solution for extracting data from PDF datasheets

The development process using Cursor AI involved:

1. **Initial Requirements Analysis**: Described the PDF structure and data extraction needs to Cursor AI
2. **Library Selection**: Cursor AI recommended appropriate Python libraries:
   - `pdfplumber` for PDF table extraction
   - `pandas` for data handling
   - `re` for pattern matching

3. **Code Implementation**: Cursor AI helped generate a Python class `OpticsDataExtractor` that:
   - Processes PDF files page by page
   - Identifies relevant data sheets
   - Extracts constants from targeted tables

## Required Libraries

- `pdfplumber`  
- `pandas`
- `re`

## Usage

1. Install the required libraries first:
```bash
pip install pdfplumber pandas
```

2. Save your PDF file containing the datasheets
3. Modify the `pdf_path` in the code to point to your PDF file
4. Run the script:
```bash
python pdf_extractor.py
```

## Conclusion

The development of this PDF data extraction tool demonstrates the efficiency of AI-assisted programming. Through iterative feedback and refinement with Cursor AI:

- The entire development process took less than 20 minutes
- Multiple iterations helped perfect the code and CSV output
- Successfully automated what would have been a tedious manual data extraction task

It's impressive to see what could be achieved with AI-assisted development tools in January 2025, turning a complex PDF parsing challenge into a straightforward automated solution in minutes.

## Note

**Important**: This code is specifically designed to work with this PDF file only:
```bash
https://www.us.schott.com/shop/medias/schott-optical-glass-collection-datasheets-english-us-march2018.pdf
```

The program is tailored to parse the specific format and structure of the Schott Optical Glass Collection datasheets (English, March 2018 version). It may not work correctly with other PDF files or even different versions of this catalog.

To use the program:
1. Download this specific PDF file
2. Save it in your project directory
3. Update the `pdf_path` in the code to point to this file
