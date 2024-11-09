# Low-Light-Image-Enhancement-for-Medical-Imaging-applications

Objective:
This research seeks to develop a robust deep learning model specifically designed to enhance low-light medical images. By focusing on medical imaging in low-resource settings or environments where optimal lighting is unavailable, this work aims to improve the diagnostic quality and usability of images in healthcare applications.

**Background and Motivation:**
Medical imaging is foundational to accurate diagnosis and effective treatment planning. However, imaging in low-light conditions can severely compromise image quality, leading to reduced clarity, contrast, and overall diagnostic value. This issue is especially prevalent in resource-limited or remote environments where specialized equipment, controlled lighting, or frequent maintenance may not be feasible. Enhancing low-light images holds the potential to address these limitations, enabling better diagnostics and healthcare outcomes across various medical disciplines.In recent years, deep learning models, particularly convolutional neural networks (CNNs), have shown significant success in image enhancement tasks, including denoising, contrast adjustment, and resolution improvement. Applying these methods to medical images captured in suboptimal lighting conditions could increase image clarity, enabling more accurate diagnoses and supporting a range of clinical applications such as telemedicine, mobile diagnostics, and emergency care.

**Modelling Image desgradtion and Noise patterns**

This involves analyzing real-world low-light images and detecting common types of noise and artifacts that often occur in such images. These include:

-**Gaussian noise**: Often caused by sensor limitations, particularly in low-light conditions.

-**Salt-and-pepper noise**: Random pixel corruption caused by transmission errors.

-**Blur**: Caused by camera motion, poor focus, or low light.

-**JPEG compression artifacts**: Blocky patterns or distortion resulting from lossy image compression.

The goal of this analysis is to quantify these distortions, enabling better understanding and potential mitigation of image degradation in low-light environments. This approach is useful in various fields, including medical imaging, astronomy, surveillance, and photography, where low-light conditions are common.

**Artifact Quantification**: 
This is the process of measuring and evaluating the severity of distortions or imperfections (artifacts) in an image, which can result from various factors such as noise, blur, or compression. It involves calculating specific numerical metrics (e.g., variance, ratio, or block differences) to objectively assess the presence and strength of these artifacts. By quantifying artifacts, one can determine the level of image degradation and guide the application of appropriate correction techniques (like denoising, deblurring, or artifact removal) to improve image quality. They are given in the table below

| **Artifact**                    | **Weak Artifact**                        | **Moderate Artifact**                           | **Strong Artifact**                           |
|---------------------------------|------------------------------------------|-------------------------------------------------|------------------------------------------------|
| **Gaussian Noise (Variance)**   | Variance < 0.01                          | 0.01 ≤ Variance ≤ 0.02                          | Variance > 0.02                               |
| **Salt-and-Pepper Noise Ratio** | Ratio < 0.02                             | 0.02 ≤ Ratio < 0.05                             | Ratio ≥ 0.05                                  |
| **Blur (Laplacian Variance)**   | Laplacian Variance > 0.05                | 0.02 ≤ Laplacian Variance ≤ 0.05                | Laplacian Variance < 0.02                     |
| **JPEG Compression Artifacts**  | Block Variance ≤ 5                       | 5 < Block Variance ≤ 10                         | Block Variance > 10                           |


The following table indicates the results of the quantification of the noise patterns for the 23 images used

    Image Name    Gaussian Noise (Variance)    Salt-and-Pepper Noise Ratio    Blur Metric    JPEG Artifact Metric
    __________    _________________________    ___________________________    ___________    ____________________

    "o1.png"               0.003453                      0.49191                0.017314          0.00042016     
    "22.png"             3.4681e-05                      0.37394                0.015022          0.00014864     
    "23.png"             8.3507e-06                      0.57271                0.012593          6.2397e-05     
    "55.png"             1.1188e-05                      0.62972                0.012244          8.2837e-05     
    "79.png"             0.00025887                      0.21197                0.016845          0.00024972     
    "146.png"            0.00042203                      0.25324                0.020662          0.00028344     
    "179.png"            0.00076562                      0.17282                0.022222          0.00028045     
    "493.png"            0.00011206                      0.81341               0.0092257          5.3556e-05     
    "547.png"            2.4191e-05                      0.33869                0.016652          0.00013797     
    "665.png"            7.6219e-05                      0.75875                0.015063          6.3197e-05     
    "669.png"            0.00043671                      0.31625                0.016487          0.00017339     
    "748.png"            5.4176e-05                      0.51404                0.020749          0.00064761     
    "778.png"            1.1674e-05                      0.74238                0.020624          0.00026988     
    "780.png"            0.00027525                      0.72166                0.019452           0.0006249     

The following overall observations can be made from the above table

**Gaussian Noise**: Most images likely have low levels of Gaussian noise, as the variance is generally below the threshold for strong artifacts.

**Salt-and-Pepper Noise**: The ratio of salt-and-pepper noise is generally low, indicating minimal random pixel corruption.

**Blur**: There is a mix of blur levels, with some images exhibiting moderate to strong blur. This could be due to various factors like camera focus, motion blur, or image processing techniques.

**JPEG Compression Artifacts**: The block variance suggests that most images have low levels of JPEG compression artifacts, indicating that they have not been heavily compressed or compressed efficiently.
