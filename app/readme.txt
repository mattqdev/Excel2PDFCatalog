# 1) create and activate a virtualenv
python -m venv .venv
# Windows
.venv\Scripts\activate
# macOS / Linux
# source .venv/bin/activate

# 2) install dependencies (if app/requirements.txt encoding causes errors,
# install the minimal set below instead)
pip install -r app/requirements.txt || true
pip install reportlab pillow pandas openpyxl