# African Cigarette Prices Analysis

## Dataset Setup for Team Members

### Prerequisites
1. Get your Kaggle API key:
   - Go to [kaggle.com](https://kaggle.com) → Your Account → API
   - Click "Create New API Token"
   - Save the downloaded `kaggle.json` file

### Running the Notebook
1. Open the notebook from this GitHub repo in Google Colab
Run the following;

!pip install kaggle
def setup_kaggle():
    from google.colab import files
    print("Please upload your kaggle.json file:")
    uploaded = files.upload(){Upload your kaggle.json file}
    
    !mkdir -p ~/.kaggle
    !mv kaggle.json ~/.kaggle/
    !chmod 600 ~/.kaggle/kaggle.json
    print("Kaggle setup complete!")

# Download dataset function
def download_dataset():
    print("Downloading African Cigarette Prices dataset...")
    !kaggle datasets download -d "waalbannyantudre/african-cigarette-prices"
    !unzip "african-cigarette-prices.zip"
    print("Dataset downloaded and extracted!")
    print("File: acp-r1-r12-2016-2022-v1.6.csv (45MB)")

# Robust dataset loading with encoding handling
import pandas as pd

def load_dataset_safely():
    file_path = 'acp-r1-r12-2016-2022-v1.6.csv'
    
    # Try common encodings
    encodings = ['latin-1', 'iso-8859-1', 'cp1252', 'utf-8', 'utf-8-sig']
    
    for encoding in encodings:
        try:
            print(f"Trying encoding: {encoding}")
            df = pd.read_csv(file_path, encoding=encoding)
            print(f"✅ Successfully loaded with encoding: {encoding}")
            return df, encoding
        except UnicodeDecodeError:
            continue
        except Exception as e:
            print(f"Other error with {encoding}: {e}")
            continue
    
    print("❌ All encodings failed")
    return None, None

# Load the dataset
df, used_encoding = load_dataset_safely()

if df is not None:
    print(f"\n📊 Dataset Information:")
    print(f"Shape: {df.shape}")
    print(f"Encoding used: {used_encoding}")
    print(f"Columns: {list(df.columns)}")
    print(f"\nFirst 5 rows:")
    display(df.head())
else:
    print("Failed to load dataset. Please check the file.")

3. Dataset file: `acp-r1-r12-2016-2022-v1.6.csv` (45MB)

### Dataset Information
- **Source**: [African Cigarette Prices on Kaggle](https://www.kaggle.com/datasets/waalbannyantudre/african-cigarette-prices)
- **Size**: ~45MB
- **Time Period**: 2016-2022
- **License**: CC BY 4.0

### Team Collaboration
- Make changes to different sections of the notebook
- Commit with clear messages describing your changes
- Pull latest changes before starting work
