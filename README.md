# Yeltech Rail Temperature Prediction Using ML
Web application to deploy and monitor ML models developed to forecast rail temperature.

## Getting Started
### Init conda environment
```sh
conda create -n yeltech-ai python=3.10
```

### Installation

1. ```sh
   pip install -r front_end/requirements.txt
   ```

2. ```sh
   docker build -t "swagger-ui" -f back_end/Dockerfile .
   ```

3. ```sh
   docker run -p 8296:8296 swagger-ui
   ```

4. ```sh
   streamlit run main.py
