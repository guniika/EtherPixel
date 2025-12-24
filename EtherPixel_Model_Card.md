# Model Card: EtherPixel-SR
Architecture Deep-Dive
* **Generator**: 5 Residual-in-Residual blocks optimized for high-frequency spatial recovery.
* **Normalization**: **Spectral Normalization** was utilized to stabilize the Discriminator against the high-albedo (brightness) variance of Himalayan snow.
* **Loss Function**: A hybrid Adversarial + MSE loss to balance pixel-perfect accuracy with perceptual sharpness.
* **Data Specs**: Sentinel-2 Top-of-Atmosphere (TOA) Reflectance, filtered for <10% cloud cover via GEE.
