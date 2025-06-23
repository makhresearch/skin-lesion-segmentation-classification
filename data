# ==============================================================================
# Final and reliable method — clean dataset structure, no .cast() required
# ==============================================================================

# Step 1: Install the Hugging Face datasets library
!pip install datasets -q

# Step 2: Download and unzip the dataset (recommended method)
import requests
from zipfile import ZipFile
from io import BytesIO
from pathlib import Path

url = "https://huggingface.co/datasets/makhresearch/skin-lesion-segmentation-classification/resolve/main/skin-lesion-segmentation-classification.zip"
print("Downloading the dataset ZIP file...")
response = requests.get(url)
response.raise_for_status()
print("✅ Download complete.")

print("\nExtracting files...")
with ZipFile(BytesIO(response.content)) as zf:
    zf.extractall(".")
print("✅✅✅ Extraction complete.")

# ==============================================================================
# Done
# ==============================================================================
