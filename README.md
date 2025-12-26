# Full-Body-Fracture-Detector
An Ensemble of AIs that can be used for a variety of fracture types

# The Problem
* Radiologists are constantly under stress
* Misdiagnoses leads to wasted time going to other visits (Not to mention the costs)
* Not every place has world-class radiologists on site
<p align="center">
 <img src = "https://outcomesrocket.health/wp-content/uploads/2020/04/Reducing-Misdiagnosis-in-Radiology-and-Beyond-1.png" width = "100%" height = "auto">
</p>

# The Solution 
### Implement AI
* Computers don't get tired. A YOLO model will look at the 1,000th image with the same focus as the 1st one. It spots the subtle patterns that a human eye might gloss over due to exhaustion.

# The Setup
### 1. The Frontend
* This is the website where the user or technician interacts with the tool. It needs a clean upload area for the X-ray. Its job is to handle the file, send it to the backend for processing, and then display the final results like the image overlays and the summary.

### 2. The Bounding Box Model (YOLO Model)
* A YOLO model determines bounding boxes for the fractures in the image. There can be multiple bounding boxes if there's multiple fractures

### 3. The Classifier
* An AI model gets fed copies of the same image, but for every fracture found, the system generates a unique copy of the original image. Specific Overlay: On "Image 1," the system draws only the first bounding box. On "Image 2," it draws only the second, and so on. These images get classified by the AI on what type of fracture is present.

### 4. The Reporter (MedGemma)
* After the detection is done, you have raw data (like coordinates and labels). This data is fed into MedGemma, a language model trained on medical text. It takes those technical results (Along with a potential clinical note) and writes a clear, professional summary that explains the findings in plain English.

### 5. The Output (Result Display)
* The final step sends everything back to the website. The user sees the original X-ray with a red box highlighting the break, the type of fracture, and the written report sitting right next to it.

# Contributors
### Thank you to
* Partho Biswas
* Ambrose Sukraj
* Alikhan Zhumabayev
* And Many Other Supporters!
