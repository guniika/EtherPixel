PROJECT VISION

Monitoring sub-hectare glacial lakes in the high-altitude Chenab Basin is critical for assessing Glacial Lake Outburst Flood (GLOF) risks. However, standard 10m Sentinel-2 imagery often obscures the fine-scale moraine dam structures and precise water-lines needed for accurate modeling.

EtherPixel is an elite Super-Resolution framework that leverages Generative Adversarial Networks (SRGANs) to "hallucinate" sub-pixel details, effectively transforming blurry satellite "blobs" into sharp, scientifically actionable 2.5m data.

CORE INNOVATION
Adversarial Reconstruction: Utilizes a Deep Generator with 5 Residual Blocks to preserve and enhance structural integrity.

Spectral Integrity: Implements Spectral Normalization to stabilize RGB channels and eliminate chromatic noise common in high-reflection snow environments.

Cloud-Native Pipeline: Integrated with the Google Earth Engine API for seamless multispectral TOA reflectance data acquisition.

Performance Benchmark: Achieved an initial PSNR (Peak Signal-to-Noise Ratio) of 27.51 dB, marking a significant leap in spatial clarity.

TECHNICAL PERFORMANCE

The model underwent 100 epochs of training on a T4 GPU, demonstrating rapid convergence and stability.

Initial Loss: 1.4908
Final Loss: 0.0088

Accuracy: 27.51 dB PSNR

Hardware: Linux-based CUDA environment

Visual Proof-of-Concept
Comparison: (Left) Original 10m Sentinel-2 Input. (Right) EtherPixel 2.5m Neural Reconstruction. Note the sharpened boundary definition between the glacial lake and the surrounding moraine.

STACK AND STANDARDS

Deep Learning: PyTorch

Remote Sensing: Google Earth Engine (GEE)

Processing: NumPy & OpenCV

Visualization: Matplotlib

RESPOSITORY STRUCTURE

models/EtherPixel.pth: Pre-trained neural weights for Himalayan terrain.

notebooks/EtherPixel_Core.ipynb: Full training and inference pipeline.

reports/Technical_Abstract.pdf: Scientific breakdown for IIT Mandi review.

FUTURE HORIZON

To further solidify EtherPixel as a tool for researchers at IIT Mandi, the next phase involves:

Scaling training to 5,000+ epochs to resolve remaining chromatic artifacts.

Integrating automated Area Estimation to track lake expansion over time.

Deploying as a lightweight web interface for real-time glaciological monitoring.
