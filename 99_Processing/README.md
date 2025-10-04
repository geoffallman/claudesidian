# 99_Processing - File Staging Area

## Purpose
Temporary workspace for files that need processing before going to their final destination in the claudesidian knowledge base.

## Workflow
1. **Drop files here** when you want Claude Code to process them
2. **Process with Claude** - read, convert, analyze, extract content
3. **Move results** to appropriate final location (Projects, Resources, etc.)
4. **Clean up** temporary files after processing

## Folder Structure
```
99_Processing/
├── documents/    # Word docs, PDFs for conversion to markdown
├── images/       # Screenshots, photos for analysis or archiving
├── data/         # Spreadsheets, CSVs for processing or analysis
└── README.md     # This file
```

## Common Use Cases

### Document Conversion
- **Word docs** → Convert to markdown for Projects or Resources
- **PDFs** → Extract text or analyze content
- **PowerPoint** → Convert slides to markdown summaries

### Image Processing
- **Screenshots** → Analyze and document findings
- **Diagrams** → Extract information and create markdown descriptions
- **Photos** → Archive with context in appropriate folders

### Data Analysis
- **Spreadsheets** → Convert to markdown tables or analysis
- **CSVs** → Process data and create summaries
- **JSON/XML** → Parse and document structure

## File Naming
Use descriptive names with date prefixes for easy organization:
- `2025-10-03_ruchika-roadmap.docx`
- `2025-10-03_screenshot-new-feature.png`
- `2025-10-03_user-survey-data.xlsx`

## Cleanup
- **Delete processed files** after moving results to final location
- **Keep folder empty** except for active processing
- **Don't commit processed files** to git (temporary workspace only)

## Examples

### Processing Ruchika's Roadmap
1. Put `ruchika-roadmap.docx` in `documents/`
2. Claude reads and converts to markdown
3. Move result to `03_Resources/People/Colleagues/Ruchika_Julapalli/projects/`
4. Delete original Word doc from processing folder

### Screenshot Analysis
1. Put screenshot in `images/`
2. Claude analyzes and creates markdown summary
3. Move summary to relevant project or resource folder
4. Archive image if needed, or delete if content captured in markdown