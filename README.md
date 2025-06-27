Smart Data Visualization Dashboard
A comprehensive web-based data visualization tool that loads datasets from AWS S3 and provides interactive plotting capabilities through an intuitive Dash interface.

Features

AWS S3 Integration: Direct data loading from S3 buckets
Multi-format Support: Handles CSV, Excel (.xlsx), and ZIP files
Interactive Visualizations: Scatter plots and bar charts with dynamic filtering
Smart Column Detection: Automatically classifies columns as categorical or numerical
Responsive UI: Bootstrap-themed interface with card-based layout
Real-time Updates: Interactive dropdowns for X-axis, Y-axis, and color coding

📋 Prerequisites

Python 3.7+
AWS Account with S3 access
Valid AWS credentials

Installation

Clone or download the project files
Install required dependencies:

bashpip install boto3 pandas dash plotly dash-bootstrap-components scipy h5py numpy python-dotenv

Set up environment variables (create a .env file):

envAWS_ACCESS_KEY_ID=your_access_key_here
AWS_SECRET_ACCESS_KEY=your_secret_key_here
📂 Project Structure
project/
├── main.py                 # Main application file
├── data_service.py         # Data loading service (referenced but not included)
├── .env                    # Environment variables (create this)
├── requirements.txt        # Python dependencies
└── README.md              # This file

Configuration
AWS S3 Setup
The application is configured to work with the IEEE DataPort bucket:

Bucket Name: ieee-dataport
Default Dataset: EV Charge Station Usage data (Sept 2018 - Aug 2019)

Supported File Formats

CSV Files: Single comma-separated value files
Excel Files: .xlsx format
ZIP Archives: Containing multiple CSV/Excel files

🚀 Usage
Basic Usage

Run the application:

bashpython main.py

Access the dashboard: Open your browser to http://localhost:8050
Interact with the visualization:

Select X-axis (categorical/date columns)
Select Y-axis (numerical columns)
Choose Key column for color coding (optional)
Switch between Scatter Plot and Bar Plot



Loading Custom Datasets
To load a different dataset from S3, modify the DEFAULT_PREFIX variable in the code:
pythonDEFAULT_PREFIX = "your/s3/file/path.xlsx"
