# Low-Light-Image-Enhancement-for-Medical-Imaging-applications
Objective:
This research seeks to develop a robust deep learning model specifically designed to enhance low-light medical images. By focusing on medical imaging in low-resource settings or environments where optimal lighting is unavailable, this work aims to improve the diagnostic quality and usability of images in healthcare applications.

Background and Motivation:
Medical imaging is foundational to accurate diagnosis and effective treatment planning. However, imaging in low-light conditions can severely compromise image quality, leading to reduced clarity, contrast, and overall diagnostic value. This issue is especially prevalent in resource-limited or remote environments where specialized equipment, controlled lighting, or frequent maintenance may not be feasible. Enhancing low-light images holds the potential to address these limitations, enabling better diagnostics and healthcare outcomes across various medical disciplines.In recent years, deep learning models, particularly convolutional neural networks (CNNs), have shown significant success in image enhancement tasks, including denoising, contrast adjustment, and resolution improvement. Applying these methods to medical images captured in suboptimal lighting conditions could increase image clarity, enabling more accurate diagnoses and supporting a range of clinical applications such as telemedicine, mobile diagnostics, and emergency care.

**Modelling Image desgradtion and Noise patterns**
This involves analyzing real-world low-light images and detecting common types of noise and artifacts that often occur in such images. These include:
-**Gaussian noise**: Often caused by sensor limitations, particularly in low-light conditions.
-**Salt-and-pepper noise**: Random pixel corruption caused by transmission errors.
-**Blur**: Caused by camera motion, poor focus, or low light.
-**JPEG compression artifacts**: Blocky patterns or distortion resulting from lossy image compression.
The goal of this analysis is to quantify these distortions, enabling better understanding and potential mitigation of image degradation in low-light environments. This approach is useful in various fields, including medical imaging, astronomy, surveillance, and photography, where low-light conditions are common.

**Artifact Quantification**: process of measuring and evaluating the severity of distortions or imperfections (artifacts) in an image, which can result from various factors such as noise, blur, or compression. It involves calculating specific numerical metrics (e.g., variance, ratio, or block differences) to objectively assess the presence and strength of these artifacts. By quantifying artifacts, one can determine the level of image degradation and guide the application of appropriate correction techniques (like denoising, deblurring, or artifact removal) to improve image quality. They are given in the table below
![image](https://github.com/user-attachments/assets/e5106de8-6550-431f-a208-f249bb728c5b)
The following table indicates the results of the quantification of the noise patterns for the 23 images used
![image](https://github.com/user-attachments/assets/0ef952d3-1aca-4548-abab-ff0680f2a9d0)
