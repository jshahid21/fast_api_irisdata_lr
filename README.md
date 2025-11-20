# fast_api_irisdata_lr

This project serves a logistic regression model trained on the Iris dataset using FastAPI.

## Features

- **API Endpoint**: Accepts four iris flower measurements (`sl`, `sw`, `pl`, `pw`) and returns a predicted class.
- **Model**: Uses a pre-trained scikit-learn logistic regression model, loaded from the `mymodel` file.
- **Tech Stack**: FastAPI, scikit-learn, joblib, Uvicorn.
- **Docker Support**: Includes a Dockerfile for containerized deployment.

## Usage

1. **Install dependencies**:  
   ```
   pip install -r requirements.txt
   ```
2. **Run the API locally**:  
   ```
   uvicorn main:app --reload
   ```
3. **Docker**:  
   Build and run the container:
   ```
   docker build -t iris-api .
   docker run -p 8000:8000 iris-api
   ```

## API Example

- **GET /**  
  Query parameters: `sl`, `sw`, `pl`, `pw` (all floats)  
  Returns:  
  ```
  {"prediction is ": <class_id>}
  ```
