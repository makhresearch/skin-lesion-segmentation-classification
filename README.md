---
license: mit
task_categories:
- object-detection
- image-segmentation
language:
- en
tags:
- skin-lesion
- medical-imaging
- yolo-format
- healthcare
- dermatology
- bounding-box
- computer-vision
pretty_name: Skin Lesion Segmentation & Classification
size_categories:
- 1K<n<10K
---
## 🔗 Usage with 🤗 Datasets Library

```python
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

```

---

# 🧠✨ Skin Lesion Segmentation & Classification Dataset

Welcome to **Skin Lesion Segmentation & Classification** — a high-quality medical dataset 🧬 focused on **dermatological image analysis** using bounding boxes and segmentation annotations. Whether you're training a model for melanoma detection or experimenting with computer vision in healthcare, this dataset is built for you! 🚀🩺

---

## 📦 Dataset Overview

🔍 This dataset follows the **YOLO-style folder structure**, ready for training in detection or segmentation tasks:

```
skin-lesion-segmentation-classification/
├── train/
│   ├── images/     # 6,675 training images
│   └── labels/     # YOLO format labels
├── valid/
│   ├── images/     # 1,911 validation images
│   └── labels/
├── test/
│   ├── images/     # 961 test images
│   └── labels/
```

📄 Each `.txt` label contains YOLO format:
```
<class_id> x1 y1 x2 y2 x3 y3 ... xn yn
```

✅ All coordinates are normalized between `0` and `1`.

---
## 🧠 Classes

The dataset supports **7 lesion categories**, labeled from ID `0` to `6`. Below is a full list of class codes, descriptions, and emojis for quick visual reference:

### 🦠 Skin Lesion Types & Description

| ID | Emoji | Code   | Full Name                                             | Description                                                                 |
|----|-------|--------|--------------------------------------------------------|-----------------------------------------------------------------------------|
| 0  | 🟤    | BKL    | Benign Keratosis                                      | Non-cancerous, often scaly skin lesions. Common and usually harmless.      |
| 1  | ⚫    | NV     | Melanocytic Nevi                                      | Regular moles formed by pigment-producing cells. Typically benign.         |
| 2  | 🟠    | DF     | Dermatofibroma                                        | Firm, small nodules under the skin caused by minor trauma. Non-cancerous.  |
| 3  | 🔴    | MEL    | Melanoma                                              | A serious and potentially life-threatening skin cancer. Early detection is critical. |
| 4  | 🔵    | VASC   | Vascular Lesion                                       | Blood vessel-related marks like angiomas. Usually red or purple.           |
| 5  | 🟣    | BCC    | Basal Cell Carcinoma                                  | The most common skin cancer. Slow-growing and rarely metastasizes.         |
| 6  | ⚠️    | AKIEC  | Actinic Keratoses / Intraepithelial Carcinoma         | Pre-cancerous lesions that may evolve into squamous cell carcinoma.        |

---

## 🧪 Tasks

- 🔳 **Object Detection** (YOLO format with normalized bounding boxes)
- 🎯 **Segmentation Approximation** (using bounding box areas)
- 📌 Potential for classification/fine-tuning tasks

---

## 📦 Dataset Size

| Split  | Images | Labels |
|--------|--------|--------|
| Train  | 6,675  | 6,675  |
| Valid  | 1,911  | 1,911  |
| Test   | 961    | 961    |
| **Total** | **9,547** | **9,547** |

---

## 📝 Notes

- All lesion images are in `.jpg` format.
- Labels are compatible with **YOLOv8** training pipelines.
- The dataset is suitable for **medical AI**, **research**, and **deep learning education**.

---

## 🧠 Use Cases

This dataset can power a wide range of AI tasks:

- 🧪 **Skin lesion detection**
- 🩻 **Medical image segmentation**
- 🤖 **Disease classification** (e.g., melanoma vs benign)
- 📊 **Benchmarking object detection models** in the medical domain

---

## 🏷️ Classes

🔢 Supports one or more lesion classes (e.g., `lesion`).  
You can edit the class list based on your labeling config.

---

## 📜 License

🆓 Open for academic and commercial use under the **[MIT License](./LICENSE)**.

---

## 🧾 Citation

If you use this dataset in your research or project, please cite:

```
@dataset{makhresearch_skin_lesion_2025,
  title     = {Skin Lesion Segmentation and Classification Dataset},
  author    = {MakhResearch},
  year      = {2025},
  url       = {https://huggingface.co/datasets/makhresearch/skin-lesion-segmentation-classification}
}
```

---

## 🤝 Contributing

🙌 Contributions, feedback, and ideas are always welcome!

Let’s build better medical AI — together. 💡🩺

---


📬 For questions, citations, or collaboration requests, visit the [Linkedin Profile](https://www.linkedin.com/in/majid-khorramgah/).
