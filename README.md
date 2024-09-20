# Flask Web App Packaging

* Flask API
* Waitress

This project is a Flask-based web application packaged for production and served with Waitress.

## File Structure
- `app/`: Directory containing the Flask application code.
  - `__init__.py`: Initializes the Flask app
  - `main.py`: App init file
- `pyproject.toml`: Configuration file
- `MANIFEST.in`: Track additional files
- `README.md`: Project details.


## Features
- **Packaging**: Perform packaging of the application and generate a build file (.whl)
- **Waitress**: Serve the web application using the build file

## Prerequisites

- Python >=3.10.7

## Build the project

### Clone the Repository

```bash
git clone https://github.com/dpralay07/python-flask-web-app-packaging.git
cd python-flask-web-app-packaging
```

### Install dependencies

```bash
pip install -r requirements.txt
```
### Build
```bash
python -m build
```
This will build the application and generate a build file (.whl) inside the dist/ directory.

## Install and run the application

### Install build
Copy the "flask_app_packaging-0.1.0-py3-none-any.whl" file from the dist/ directory and move to the deployment directory. 

Install the build with the following command:
```bash
pip install flask_app_packaging-0.1.0-py3-none-any.whl
```

### Serve the application
Execute the following command:
```bash
waitress-serve --port=80 app.main:app
```
The Flask API will be available at `http://<your_ip_address>:80`

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing
Contributions are welcome! Please open an issue or submit a pull request to improve this project.

## Contact
For any questions or feedback, please contact [pralaykumar.daz@gmail.com](mailto:pralaykumar.daz@gmail.com).