python3.10 -m venv .venv
source .venv/bin/activate
python -m pip install -r requirements.txt

deactivate
source .venv/bin/activate

nodeenv -p
npm install -D tailwindcss
uvicorn main:app --port 8000 --reload
npx tailwindcss -i ./static/css/input.css -o ./static/css/style.css --watch