<div align="center">

<img src="assets/banner.svg" alt="Awesome Lens Calibration Software Banner" width="100%" />

# 📸 Awesome Lens Calibration Software 🔭

[![Awesome](https://img.shields.io/badge/Awesome-%E2%9C%94-blueviolet?style=flat-square&logo=github)](https://github.com/ishandutta2007/Awesome-Awesome-Awesome)<a href="https://discord.gg/jc4xtF58Ve"><img src="https://img.shields.io/badge/Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white" alt="Discord" /></a>
[![GitHub Stars](https://img.shields.io/github/stars/ishandutta2007/Awesome-Lens-Calibration-Software?style=flat-square&logo=github&color=gold)](https://github.com/ishandutta2007/Awesome-Lens-Calibration-Software/stargazers)
[![GitHub Forks](https://img.shields.io/github/forks/ishandutta2007/Awesome-Lens-Calibration-Software?style=flat-square&color=blue)](https://github.com/ishandutta2007/Awesome-Lens-Calibration-Software/network/members)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg?style=flat-square)](https://github.com/ishandutta2007/Awesome-Lens-Calibration-Software/blob/main/LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](https://github.com/ishandutta2007/Awesome-Lens-Calibration-Software/pulls)
<a href="https://github.com/ishandutta2007"><img alt="GitHub followers" src="https://img.shields.io/github/followers/ishandutta2007?label=Follow" /></a>

**A curated index of top SaaS products, enterprise platforms, and open-source libraries for lens calibration, optical distortion correction, chromatic aberration removal, vignetting elimination, and camera intrinsic profiling.**

[Market Overview](#-sector-overview--market-dynamics) • [SaaS & Commercial Platforms](#-saas--commercial-platforms) • [Open-Source Projects](#-open-source-github-projects) • [Key Concepts](#-key-concepts--calibration-terminology) • [Support](#-support) • [Star History](#-star-history)

</div>

---

## 📖 Introduction & SEO Overview

Every optical lens introduces physical imperfections: **barrel, pincushion, and mustache radial distortion**, **transversal (lateral) chromatic aberration**, **sensor-plane light falloff (vignetting)**, and **tangential/decentering misalignment**. High-precision photography, professional cinematography, drone photogrammetry, autonomous robotics, and computer vision (SLAM) depend on software calibration to characterize optical flaws and mathematically rectify raw pixel arrays.

This directory tracks the leading **SaaS/commercial suites** and **open-source tools** spanning target-based calibration (checkerboards, ChArUco, circle grids), straight-line scene optimization, and community-driven lens profile databases (Lensfun, Adobe `.lcp`).

---

## 📊 Sector Overview & Market Dynamics

The global camera calibration and optical alignment software market is valued at approximately **$13.45 billion to $13.75 billion**, projected to scale to **$24.8 billion by 2032** at an **8.9% CAGR**, alongside a broader industrial optical measurement and metrology software market valued between **$3.5 billion and $7.0 billion**. 

At the macro industry level, the sector is **moderately fragmented** across disparate application domains (consumer RAW photography editing, drone photogrammetry, industrial QA, and autonomous robotics). However, individual verticals exhibit **intense oligopolistic concentration**: Adobe commands a near winner-take-most position in mainstream photo editing workflows; DxO Labs and Capture One maintain an entrenched high-end studio duopoly; and Imatest functions as the de facto enterprise standard for optoelectronic hardware testing.

---

## 🏢 SaaS & Commercial Platforms

The following commercial and desktop-licensed suites provide dedicated lens profiling, automatic optical aberration correction, and camera characterization. Tiers are sorted in **descending order by company valuation / annual revenue**.

| Platform & Provider | Company Valuation / Revenue | Specific Starting Pricing | Free Tier / Trial Limits | Key Capabilities & Primary Focus |
| :--- | :--- | :--- | :--- | :--- |
| [Adobe Camera Raw & Lens Profile Creator](https://helpx.adobe.com/camera-raw/digital-negative.html) <br><sub>*(Adobe Inc. - NASDAQ: ADBE)*</sub> | **$215 Billion** Valuation <br><sub>($21.4B Annual Revenue)</sub> | **$9.99 / month** <br><sub>(Photography Plan 20GB; or $19.99/mo for Lightroom 1TB)</sub> | **7-day free trial** with full feature access to Photoshop/Lightroom; standalone **Adobe Lens Profile Creator** utility is **100% free forever** *(requires ACR/Lightroom to apply profiles)* | Industry reference checkerboard calibration utility generating `.lcp` profiles characterizing geometric radial distortion, lateral chromatic aberration, and vignetting across Adobe Camera Raw, Lightroom, and Photoshop. |
| [Capture One Pro](https://www.captureone.com/) <br><sub>*(Capture One A/S / Axcel)*</sub> | **$215 Million** Valuation <br><sub>(~$30M–$35M Annual Revenue)</sub> | **$24.00 / month** <br><sub>(or $179.00/year billed annually; $299.00 perpetual license)</sub> | **30-day fully functional free trial** <br><sub>(no credit card required; all RAW profiling and tethering tools unlocked)</sub> | Studio-grade raw workflow engine featuring factory-calibrated optical profiles for 500+ lens/body pairings, correcting geometric distortion, light falloff, and chromatic aberration with custom slider fine-tuning. |
| [Topaz Photo AI](https://www.topazlabs.com/topaz-photo-ai) <br><sub>*(Topaz Labs LLC)*</sub> | **~$120 Million** Valuation <br><sub>(~$25M–$30M Annual Revenue)</sub> | **$199.00 one-time** <br><sub>(includes 12 months of updates; optional $99/year renewal thereafter)</sub> | **Unlimited duration free trial** <br><sub>(complete UI and processing access; exported images contain a prominent watermark)</sub> | Deep learning-enhanced optical correction, automated lens distortion rectification, intelligent de-mosaicing, and AI-powered chromatic fringe suppression. |
| [DxO PhotoLab Elite](https://www.dxo.com/dxo-photolab/) <br><sub>*(DxO Labs)*</sub> | **~$80 Million** Valuation <br><sub>(~$18M–$25M Annual Revenue)</sub> | **$229.99 one-time** <br><sub>(PhotoLab Elite; or $139.99 for PhotoLab Essential perpetual)</sub> | **30-day fully functional free trial** <br><sub>(no watermark, no credit card required; unrestricted access to DxO Optics Modules)</sub> | Renowned optical laboratory calibration modules delivering per-pixel correction for geometric barrel/pincushion distortion, vignetting falloff, chromatic aberration, and edge-to-edge sharpness optimization. |
| [Imatest Master](https://www.imatest.com/) <br><sub>*(Imatest LLC)*</sub> | **~$60 Million** Valuation <br><sub>(~$15M–$20M Annual Revenue)</sub> | **$2,960.00 / year** <br><sub>(Node-locked subscription; or $8,100.00 one-time perpetual license)</sub> | **15-day free trial** <br><sub>(full access to SFRplus, eSFR ISO, and distortion testing modules; save/export functions restricted)</sub> | Industrial and aerospace benchmark software for camera and lens quality assurance; calculates SMIA TV distortion, radial distortion polynomial coefficients, grid target alignment, and MTF resolution curves. |
| [Agisoft Metashape](https://www.agisoft.com/) <br><sub>*(Agisoft LLC)*</sub> | **~$45 Million** Valuation <br><sub>(~$10M–$15M Annual Revenue)</sub> | **$179.00 one-time** <br><sub>(Standard Edition; or $3,499.00 for Professional Edition perpetual)</sub> | **30-day full-featured trial license** <br><sub>(available upon email registration; all export/saving capabilities fully operational)</sub> | Photogrammetric camera calibration suite estimating Brown-Conrady physical distortion coefficients ($k_1-k_4, p_1, p_2, b_1, b_2$) from checkerboards or scene bundle adjustment. |

---

## 💻 Open-Source GitHub Projects

Curated open-source repositories for camera calibration, optical distortion correction, and lens profiling, sorted in **descending order by GitHub star count** 🌟.

### 1. 🔭 [COLMAP](https://github.com/colmap/colmap) [![Stars](https://img.shields.io/github/stars/colmap/colmap?style=social&color=white)](https://github.com/colmap/colmap/stargazers)
- **Primary Focus**: Structure-from-Motion (SfM) and Multi-View Stereo (MVS) with full camera self-calibration.
- **Key Features**: Automates intrinsic camera parameter estimation ($f_x, f_y, c_x, c_y$) and non-linear radial/fisheye distortion modeling across unconstrained image sets without requiring checkerboard targets.
- **License**: BSD-3-Clause

### 2. 🌀 [Gyroflow](https://github.com/gyroflow/gyroflow) [![Stars](https://img.shields.io/github/stars/gyroflow/gyroflow?style=social&color=white)](https://github.com/gyroflow/gyroflow/stargazers)
- **Primary Focus**: Hardware-accelerated video stabilization using IMU telemetry with integrated lens calibration.
- **Key Features**: Features an intuitive graphical lens calibration wizard that analyzes checkerboard patterns to generate custom lens distortion profiles, calculating optical centers and focal lengths for action cameras and cinema lenses.
- **License**: GPL-3.0

### 3. 🤖 [Kalibr](https://github.com/ethz-asl/kalibr) [![Stars](https://img.shields.io/github/stars/ethz-asl/kalibr?style=social&color=white)](https://github.com/ethz-asl/kalibr/stargazers)
- **Primary Focus**: Multi-camera and visual-inertial calibration toolbox from ETH Zurich Autonomous Systems Lab.
- **Key Features**: High-precision non-linear least-squares optimization for camera intrinsic/extrinsic parameters, spatial and temporal IMU-camera offsets, and dedicated modeling for rolling-shutter cameras using AprilTag grids.
- **License**: BSD-3-Clause

### 4. 📐 [CamOdoCal](https://github.com/hengli/camodocal) [![Stars](https://img.shields.io/github/stars/hengli/camodocal?style=social&color=white)](https://github.com/hengli/camodocal/stargazers)
- **Primary Focus**: Automatic intrinsic and extrinsic calibration of multi-camera rigs and visual odometry.
- **Key Features**: Comprehensive support for generic camera models including standard pinhole, Scaramuzza omnidirectional/catadioptric, and Kannala-Brandt fisheye distortion models.
- **License**: BSD-3-Clause

### 5. 🎯 [CameraCalibration](https://github.com/dyfcalid/CameraCalibration) [![Stars](https://img.shields.io/github/stars/dyfcalid/CameraCalibration?style=social&color=white)](https://github.com/dyfcalid/CameraCalibration/stargazers)
- **Primary Focus**: Normal and fisheye camera intrinsic/extrinsic calibration.
- **Key Features**: Generates 360-degree surround-view Bird's-Eye-View (BEV) camera systems; implements checkerboard corner extraction, distortion removal, and perspective transformation.
- **License**: Apache-2.0

### 6. 📚 [Lensfun](https://github.com/lensfun/lensfun) [![Stars](https://img.shields.io/github/stars/lensfun/lensfun?style=social&color=white)](https://github.com/lensfun/lensfun/stargazers)
- **Primary Focus**: The de facto open-source photographic lens database and correction engine.
- **Key Features**: Community-maintained XML database characterizing thousands of lenses; provides C++ algorithms correcting transversal chromatic aberration, poly3/poly5/PTLens radial distortion, and cosine-falloff vignetting. Powers Darktable, RawTherapee, and DigiKam.
- **License**: LGPL-3.0

### 7. 🔬 [camera_calibration](https://github.com/puzzlepaint/camera_calibration) [![Stars](https://img.shields.io/github/stars/puzzlepaint/camera_calibration?style=social&color=white)](https://github.com/puzzlepaint/camera_calibration/stargazers)
- **Primary Focus**: Highly accurate geometric camera calibration with generic camera models.
- **Key Features**: Implements both parametric polynomial models and continuous B-spline non-parametric distortion fields for ultra-high-precision optical alignment and sub-pixel corner optimization.
- **License**: BSD-3-Clause

### 8. 🛰️ [mrcal](https://github.com/dkogan/mrcal) [![Stars](https://img.shields.io/github/stars/dkogan/mrcal?style=social&color=white)](https://github.com/dkogan/mrcal/stargazers)
- **Primary Focus**: NASA JPL's next-generation camera modeling and calibration framework.
- **Key Features**: Eliminates rigid parametric distortion formulas in favor of flexible non-linear splined surfaces; delivers formal uncertainty quantification propagation for robotics and orbital vision.
- **License**: Apache-2.0

### 9. 🐍 [lensfunpy](https://github.com/letmaik/lensfunpy) [![Stars](https://img.shields.io/github/stars/letmaik/lensfunpy?style=social&color=white)](https://github.com/letmaik/lensfunpy/stargazers)
- **Primary Focus**: Python C-extension wrapper for the Lensfun library.
- **Key Features**: Provides clean NumPy array interfacing for batch programmatic lens distortion rectification, vignetting removal, and chromatic aberration correction directly in scientific Python pipelines.
- **License**: MIT

### 10. 📏 [LensDistortionFromLines](https://github.com/alicevision/LensDistortionFromLines) [![Stars](https://img.shields.io/github/stars/alicevision/LensDistortionFromLines?style=social&color=white)](https://github.com/alicevision/LensDistortionFromLines/stargazers)
- **Primary Focus**: AliceVision's straight-line-based lens distortion rectification.
- **Key Features**: Iterative non-linear optimization computing two-parameter radial distortion models directly from straight-line scene geometry (architectural lines, horizons) without requiring physical calibration targets.
- **License**: MPL-2.0

### 11. 🎨 [GIMP-Lensfun](https://github.com/seebk/GIMP-Lensfun) [![Stars](https://img.shields.io/github/stars/seebk/GIMP-Lensfun?style=social&color=white)](https://github.com/seebk/GIMP-Lensfun/stargazers)
- **Primary Focus**: Interactive desktop GIMP plugin integrating the Lensfun correction engine.
- **Key Features**: Detects camera body and lens metadata from EXIF and applies real-time interactive previews for lens distortion, vignetting falloff, and chromatic aberration correction inside GIMP.
- **License**: GPL-3.0

### 12. 👁️ [lens-distortion-rectification](https://github.com/bbenligiray/lens-distortion-rectification) [![Stars](https://img.shields.io/github/stars/bbenligiray/lens-distortion-rectification?style=social&color=white)](https://github.com/bbenligiray/lens-distortion-rectification/stargazers)
- **Primary Focus**: Blind radial distortion rectification exploiting line straightness.
- **Key Features**: MATLAB implementation optimizing radial curvature metrics on natural images without calibration targets or prior camera parameters.
- **License**: MIT

### 13. 🎛️ [opencv_live_distortion](https://github.com/vwvw/opencv_live_distortion) [![Stars](https://img.shields.io/github/stars/vwvw/opencv_live_distortion?style=social&color=white)](https://github.com/vwvw/opencv_live_distortion/stargazers)
- **Primary Focus**: Real-time OpenCV distortion experimentation utility.
- **Key Features**: Python and OpenCV tool featuring live GUI sliders for radial ($k_1, k_2, k_3$) and tangential ($p_1, p_2$) coefficients to immediately inspect undistortion grids.
- **License**: MIT

---

## 🧠 Key Concepts & Calibration Terminology

Understanding lens calibration requires familiarity with the standard optical distortion and projective geometry models:

* **Radial Distortion**:
  * **Barrel Distortion ($k_1 < 0$)**: Image magnification decreases with distance from the optical axis; straight lines bow outward like a barrel (common in wide-angle and fisheye lenses).
  * **Pincushion Distortion ($k_1 > 0$)**: Image magnification increases with distance from the optical axis; lines bow inward toward the center (common in telephoto lenses).
  * **Mustache (Complex) Distortion**: Non-linear mix where barrel distortion dominates near the optical center and flips to pincushion distortion near the frame periphery.
* **Tangential (Decentering) Distortion ($p_1, p_2$)**:
  * Arises when physical lens elements are not perfectly parallel to each other or to the camera sensor plane, displacing pixels tangential to concentric rings.
* **Chromatic Aberration (Color Fringing)**:
  * **Transversal / Lateral Chromatic Aberration (TCA)**: Wavelength-dependent magnification differences resulting in color fringes (red/cyan, blue/yellow) near high-contrast frame edges. Fully correctable by software scaling of individual color planes.
  * **Longitudinal / Axial Chromatic Aberration (LoCA)**: Different wavelengths focus at different focal depths along the optical axis, creating purple/green halos in out-of-focus highlights.
* **Vignetting (Light Falloff)**:
  * Reduction of image brightness toward the periphery caused by lens barrels physically blocking off-axis light (mechanical vignetting), pupil geometry (optical vignetting), or the natural optical $\cos^4(\theta)$ illumination drop.
* **Camera Intrinsic Matrix ($K$)**:
  $$K = \begin{bmatrix} f_x & s & c_x \\ 0 & f_y & c_y \\ 0 & 0 & 1 \end{bmatrix}$$
  * $f_x, f_y$: Effective focal lengths in pixel units.
  * $c_x, c_y$: Principal point (optical center coordinate on the sensor).
  * $s$: Skew factor between the sensor axes (typically 0 for modern square-pixel sensors).

---

## 🤝 How to Contribute

Contributions, new tools, and updated profile libraries are welcome!

1. Fork this repository: `https://github.com/ishandutta2007/Awesome-Lens-Calibration-Software`
2. Create a feature branch: `git checkout -b add-calibration-tool`
3. Add your entry under either [SaaS & Commercial Platforms](#-saas--commercial-platforms) or [Open-Source Projects](#-open-source-github-projects).
4. Maintain exact table formatting, specific pricing figures, and verified GitHub star badges.
5. Submit a Pull Request with a clear description of the project.

---

## 💖 Support

A huge thank you to everyone exploring, contributing to, and supporting **Awesome Lens Calibration Software**! 🙌 If you found this curated directory helpful for your photography setups, drone photogrammetry pipelines, or computer vision research, please consider supporting the project:

- ⭐ **Star this repository** to boost discovery and help more developers, photographers, and researchers find it.
- 🍴 **Fork & Share** with your colleagues, lab teams, and photography communities.
- 🛠️ **Contribute entries** to keep the optical correction libraries, lens profile databases, and camera tools continually updated.
- ☕ **Buy Me a Coffee**: If this repository saved you research hours or helped solve tricky optical distortions, you can support future development and maintenance via the [GitHub Sponsors Dashboard](https://github.com/sponsors/ishandutta2007).

<p align="center">
  <a href="https://github.com/sponsors/ishandutta2007">
    <img src="https://img.shields.io/badge/Sponsor-%E2%9D%A4-ea4aaa?style=for-the-badge&logo=github-sponsors" alt="Sponsor on GitHub" />
  </a>
  &nbsp;&nbsp;
  <a href="https://github.com/sponsors/ishandutta2007">
    <img src="https://img.shields.io/badge/Buy%20Me%20A%20Coffee-FFDD00?style=for-the-badge&logo=buy-me-a-coffee&logoColor=black" alt="Buy Me A Coffee" />
  </a>
</p>

---

## ⭐ Star History

[![Star History Chart](https://star-history.dera.page/sv?repos=ishandutta2007/Awesome-Lens-Calibration-Software&type=date&legend=top-left)](https://star-history.dera.page/#ishandutta2007/Awesome-Lens-Calibration-Software&type=date&legend=top-left)

---

## 📜 Disclaimer & License

- This compilation is community-curated for informational, educational, and research purposes. Product names and trademarks belong to their respective copyright holders.
- Distributed under the [MIT License](LICENSE).
