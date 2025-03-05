# <img src="https://github.com/manvendrasingh09/PixelScan/blob/main/Resources/PixelScan.png" alt="PixelScan Logo" width="30" style="vertical-align: middle;"/> PixelScan: Image Deepfake Detection



## Overview

This repository showcases the research titled **"Countering Deepfakes using an Improved Advanced CNN and its Ensemble with Pretrained Models"**, published at the **Third International Conference on Electrical, Electronics, Information, and Communication Technologies (ICEEICT 2024)**.

The project, named **PixelScan** is a sophisticated model designed to detect and mitigate the spread of DeepFake images online. Using an ensemble of Advanced CNN, MobileNet, and Xception architectures, the model achieves a **97.89% accuracy** in detecting DeepFakes. This repository provides a comprehensive overview of the methodology, datasets, and results but does **not** share the source code.

---

## Authors

- **Abeer Mathur**
    [LinkedIn](https://in.linkedin.com/in/abeermathur)
- **Kshitiz Bhargava**
    [LinkedIn](https://in.linkedin.com/in/kshitiz-bhargava)
- **Manvendra Singh**
    [LinkedIn](https://www.linkedin.com/in/manvendrasingh09/)
- **Moulik Tejpal**
    [LinkedIn](https://in.linkedin.com/in/mouliktejpal)
- **Krishnaraj Natarajan**
    [LinkedIn](https://in.linkedin.com/in/krishnaraj-natarajan-71b8a658)

> Affiliation: Department of Software Systems, School of Computer Science & Engineering, Vellore Institute of Technology, Vellore, India.  
> Contact Emails: abeermathur17@gmail.com, kshitizbhargava2626@gmail.com, m.s.jaunpur@gmail.com, moulik.tejpal@gmail.com, krishnarajtce@gmail.com

---

## Project Highlights

- **Problem Addressed:** The rise of DeepFake images poses risks such as misinformation, blackmail, and propaganda.
- **Solution Provided:** PixelScan introduces a novel ensemble detection model combining:
  - **Advanced CNN (ACNN)** - A custom-built convolutional architecture.
  - **MobileNet** - A lightweight pretrained CNN.
  - **Xception** - A robust pretrained model for image classification.
- **Key Achievement:** The ensemble model achieved **97.89% accuracy**, outperforming standalone models.

---

## Research Paper

[IEEE Paper](https://ieeexplore.ieee.org/document/10718622)
- Abstract:  
   > The extensive spread of DeepFake images on the internet has emerged as a significant challenge, with applications ranging from harmless entertainment to harmful acts like blackmail, misinformation, and spreading false propaganda. To tackle this issue, this paper introduces a sophisticated DeepFake detection model designed to identify and mitigate the increase of these deceptive images. The model architecture integrates an ensemble approach, combining the strengths of two pretrained Convolutional Neural Network (CNN) models—MobileNet and Xception—with a novel CNN architecture, the Advanced CNN (ACNN). This rigorous validation process enabled the model to achieve a high accuracy rate of 97.89% in detecting DeepFakes.

---

## Website & Application

Access the **PixelScan** application and website here: [PixelScan](https://pixelscan.site)  
From this website, users can download the app and explore its features for DeepFake detection.

---

## Methodology

### Proposed Architecture
The ensemble model combines:
1. **Advanced CNN (ACNN)**:
   - Custom-designed convolutional layers for efficient feature extraction.
   - Efficient processing with pooling, dropout, and batch normalization.
   - Binary cross-entropy loss with Adam optimizer for robust training.
2. **MobileNet**:
   - Pretrained lightweight CNN optimized for mobile applications.
3. **Xception**:
   - Depthwise separable convolutions for advanced feature recognition.

### Ensemble Mechanism
- Each model independently classifies the input image as real or fake.
- Predictions are aggregated using a **majority voting mechanism** to ensure reliability.

### Datasets Used
1. **140k Real and Fake Faces Dataset**:
   - Real images: Nvidia’s Flickr collection.
   - Fake images: StyleGAN-generated images.
   - Augmented with rotations, brightness changes, and cropping for diversity.
2. **Fake-vs-Real Faces (Hard)**:
   - Real images: Unsplash API (processed with OpenCV).
   - Fake images: StyleGAN2 from "thispersondoesnotexist.com".

---

## Results

### Individual Model Performance
| Model          | Accuracy | Precision | Recall |
|----------------|----------|-----------|--------|
| Advanced CNN   | 98%      | 97%       | 98%    |
| MobileNet      | 99%      | 99%       | 99%    |
| Xception       | 99%      | 99%       | 99%    |

### Ensemble Performance
- **Accuracy:** 97.89%
- **Precision:** 97.29%
- **Recall:** 98.52%
- **F1-Score:** 97.90%
- **ROC-AUC:** 0.996

### Evaluation Metrics
- Confusion Matrix:
  - True Positives: 9762
  - True Negatives: 9852
  - False Positives: 274
  - False Negatives: 148
- Performance curves:
  - ROC Curve: AUC = 0.996
  - Precision-Recall Curve: AUC = 0.9952

---

## Figures & Visuals

### Ensemble Model
![Ensemble Model](https://github.com/manvendrasingh09/PixelScan/blob/main/Resources/Ensemble%20Model.png) 

### Sequential Diagram
![Sequential Diagram](https://github.com/manvendrasingh09/PixelScan/blob/main/Resources/Sequential%20Diagram.png) 

### Performance Graphs

1. **Confusion Matrix**  
   The confusion matrix showcases the high number of true positives and true negatives, reflecting the model's reliability in DeepFake detection.
   
   <img src="https://github.com/manvendrasingh09/PixelScan/blob/main/Resources/Confusion%20Matrix.png" width="500"/>

3. **Training Accuracy**  
   The ACNN model's training accuracy started at 50% and steadily improved, reaching 98% by the final epoch.
   
   <img src="https://github.com/manvendrasingh09/PixelScan/blob/main/Resources/ACNN%20Training%20Accuracy.png" width="500"/>

5. **Training Loss**  
   The ACNN model's training loss started at 1.6 and decreased to 0.07, showing effective learning during training.
   
   <img src="https://github.com/manvendrasingh09/PixelScan/blob/main/Resources/ACNN%20Training%20Loss.png" width="500"/>

7. **Precision-Recall Curve**  
   The precision-recall curve with an area of 1.00 demonstrates the ensemble model's capability to maintain high precision and recall across all thresholds.
   
   <img src="https://github.com/manvendrasingh09/PixelScan/blob/main/Resources/Precision-Recall%20Curve.png" width="500"/>

9. **ROC Curve**  
   The ROC curve with an area of 1.00 highlights the strong performance of the ensemble model in distinguishing between real and DeepFake images.
   
   <img src="https://github.com/manvendrasingh09/PixelScan/blob/main/Resources/ROC%20Curve.png" width="500"/>

---

## How to Use

1. Visit [PixelScan](https://pixelscan.site) to download the application.
2. Upload your image to the app.
3. Get a classification result indicating whether the image is real or fake.

---
## **Run Locally with [Docker](https://hub.docker.com/r/kshitizb/pixelscan)**

### **1. Pull the Docker Image**
To download the latest version of `pixelscan` from Docker Hub, run:

```bash
docker pull kshitizb/pixelscan:latest
```

### **2. Run the Container**
Start the container and expose it on port **8000**:

```bash
docker run -d -p 8000:8000 --name pixelscan --restart unless-stopped kshitizb/pixelscan:latest
```

### **3. Access the API**
Once the container is running, open a browser and go to:

```
http://<your-server-ip>:8000
```

Or test via **FastAPI interactive docs**:

```
http://<your-server-ip>:8000/docs
```

---

## **Endpoints**
| Method  | Endpoint       | Description |
|---------|---------------|-------------|
| **GET** | `/`           | Homepage - Image Upload Form |
| **POST** | `/upload/`   | Upload and classify an image |

---

## Acknowledgments

We express our gratitude to:
- Colleagues and mentors for insightful discussions and guidance.
- VIT University for their support during this research.

---

## License

This repository is for academic reference only.  
The source code for the project is proprietary and not included in this repository.

---

## Citation

If you use this work in your research, please cite it as follows:

### APA
Mathur, A., Bhargava, K., Singh, M., Tejpal, M., & Natarajan, K. (2024). Countering Deepfakes using an Improved Advanced CNN and its Ensemble with Pretrained Models. *Third International Conference on Electrical, Electronics, Information, and Communication Technologies (ICEEICT 2024)*. DOI: [10.1109/ICEEICT61591.2024.10718622](https://ieeexplore.ieee.org/document/10718622)

### MLA
Mathur, Abeer, et al. "Countering Deepfakes using an Improved Advanced CNN and its Ensemble with Pretrained Models." *Third International Conference on Electrical, Electronics, Information, and Communication Technologies (ICEEICT 2024)*, 2024, DOI: [10.1109/ICEEICT61591.2024.10718622](https://ieeexplore.ieee.org/document/10718622).

### IEEE
A. Mathur, K. Bhargava, M. Singh, M. Tejpal, and K. Natarajan, "Countering Deepfakes using an Improved Advanced CNN and its Ensemble with Pretrained Models," *Third International Conference on Electrical, Electronics, Information, and Communication Technologies (ICEEICT 2024)*, 2024, DOI: [10.1109/ICEEICT61591.2024.10718622](https://ieeexplore.ieee.org/document/10718622).

### BibTeX
```bibtex
@inproceedings{Mathur2024,
  author    = {Mathur, Abeer and Bhargava, Kshitiz and Singh, Manvendra and Tejpal, Moulik and Natarajan, Krishnaraj},
  title     = {Countering Deepfakes using an Improved Advanced CNN and its Ensemble with Pretrained Models},
  booktitle = {Third International Conference on Electrical, Electronics, Information, and Communication Technologies (ICEEICT 2024)},
  year      = {2024},
  doi       = {10.1109/ICEEICT61591.2024.10718622},
  url       = {https://ieeexplore.ieee.org/document/10718622}
}
```
---
