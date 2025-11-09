# Excel2PDFCatalog

Excel2PDFCatalog is a Python tool that reads product/catalog data from an Excel file and generates one PDF catalog. It provides a minimal UI to select the Excel file and image folders and a PDF builder that composes pages from rows and linked images.

## ✨ Key Features

- Excel parsing powered by ***pandas*** and ***openpyxl***.
- Configurable column-to-field mapping to adapt to different Excel formats.
- Customizable PDF generation using reportlab.
- Per-product image support: each row can link to dedicated image folders.
- Minimal UI for selecting inputs/outputs and starting the process.
- Settings stored in JSON configuration files.

## 🛠️ Requirements

- **Python 3.8+**
- Dependencies listed in app/requirements.txt (notably: reportlab, pillow, pandas, openpyxl)

## 🚀 Installation & Run (Windows)

### 1. Create and activate a virtual environment
```bash
python -m venv .venv
.venv\Scripts\activate
```

### 2. Install dependencies
```bash
pip install -r app/requirements.txt
```

### 3. Run the application
```bash
python Excel2PDFCatalog.py
```

👉 Alternatively, launch directly via VS Code using ``.vscode/launch.json``

## ⚙️ Configuration

``app/config.json`` → runtime defaults and options.

``Excel2PDFCatalog.config`` → column mapping and project-specific rules.

Edit these files to match your Excel layout, image folder structure, and output preferences.

📂 Project Structure

```bash
Excel2PDFCatalog/
├── Excel2PDFCatalog.py        # Main entrypoint (UI + workflow)
├── app/
│   ├── config_utils.py        # Configuration management
│   ├── ui_interface.py        # UI logic
│   ├── build_PDF.py           # PDF generation (build_pdf function)
│   └── requirements.txt       # Dependencies
├── img_products/              # Product images
├── img_general/               # General images
├── example_excel/             # Example Excel files
├── example_catalog/           # Example PDF catalogs
└── fonts/                     # Custom fonts
```

## ▶️ Usage

1. Start the application.
2. Select the Excel file and image folder(s) via the UI.
3. Set the output folder and other options if needed.
4. Click Go → the PDF catalog is generated in the configured folder.

## 📄 Preview

An Excel file with columns Name, Price, Image can produce a PDF catalog with:

- Product title
- Formatted price
- Linked image from img_products/

### UI Preview (Windows):
<img src="https://github.com/alexscarcella/Excel2PDFCatalog/blob/main/assets/Preview_Windows.png?raw=true" alt="Windows UI Screenshot" width="80%">

### UI Preview (MacOS)
<img src="https://github.com/alexscarcella/Excel2PDFCatalog/blob/main/assets/Preview_MacOS.png?raw=true" alt="MacOS UI Screenshot" width="80%">

## 🛠️ Troubleshooting

- Ensure image references in Excel match filenames in the provided folders.
- If library errors occur, reinstall dependencies inside the active virtual environment.
- Check the VS Code terminal/output for detailed error messages.

## 🤝 Contributing

Report bugs or suggest improvements by opening an Issue.

Submit Pull Requests for new features or optimizations.

Improve documentation and examples to help other users.

## 📌 Notes

This project is intended as an internal, editable tool. You can adapt the code and configuration files to fit specific catalog formats or layout requirements.