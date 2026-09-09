# Automating Python Projects with Pip, PyPi & Scripting

A small Python automation tool that fetches data from a public API and writes a timestamped log file.

## What it does

- `generate_log(data)` --> validates that `data` is a list, then writes each entry to a file named `log_YYYYMMDD.txt` (today's date), one entry per line. Returns the filename.
- `fetch_data()` --> uses the `requests` package to call a public test API (`jsonplaceholder.typicode.com`) and returns the JSON response.
- Running the script directly (`if __name__ == "__main__":`) fetches a sample post and generates a sample log file, demonstrating both functions together.

## Setup

1. Clone the repo and navigate into it:
```bash
   git clone https://github.com/hanjennings1/course-7-module-6-pip-pypi-scripting-lab
   cd course-7-module-6-pip-pypi-scripting-lab
```
2. Install dependencies with pipenv:
```bash
   pipenv install --dev
   pipenv shell
```

## Usage

Run the script directly:
```bash
python lib/generate_log.py
```

This prints the fetched API post title and writes a log file (e.g. `log_20260909.txt`) to the current directory.

## Testing

Run the test suite with:
```bash
pytest testing/test_generate_log.py -v
```

## Dependencies

Tracked in `requirements.txt`, generated via:
```bash
pip freeze > requirements.txt
```