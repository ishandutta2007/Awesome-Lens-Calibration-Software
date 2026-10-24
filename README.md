# Awesome-Lens-Calibration-Software

# Top Lens Calibration Software Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**  
*Focused on Distortion Correction, Vignetting Removal & Open Lens Profile Databases*  
**Last updated: March 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Lens Calibration Software**. These tools characterize and correct the optical imperfections inherent to every lens — barrel and pincushion distortion, lateral chromatic aberration, and vignetting — by generating profiles from calibration targets or applying corrections from open databases, with a spectrum running from Adobe's proprietary profile creator to open-source libraries like Lensfun that power correction across darktable, RawTherapee, and digiKam.

**Examples** include Lensfun, Hugin Calibrate Lens GUI, PTLens/clens, and gyroflow (the category leaders).

**Open-source emphasis**: This section is heavily expanded with every major active project for self-hosting, open profile databases, and transparent correction algorithms — especially relevant as **Lensfun remains the de facto standard library for lens correction in open-source photography**, and **Hugin's calibrate_lens_gui** provides a GUI-driven straight-line calibration workflow without proprietary tooling .

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **Adobe Lens Profile Creator** — **The reference tool for creating custom Adobe lens profiles.** **Freeware for Windows** (79.8 MB installer) , used to generate `.lcp` profiles for Adobe Camera Raw, Lightroom, and Photoshop . **Workflow**: capture a set of checkerboard images with the specific camera and lens, convert raw files to DNG using Adobe Camera Raw, then import into Lens Profile Creator to characterize geometric distortion, lateral chromatic aberration, and vignetting . **Trade-offs**: Windows-only, requires the Adobe ecosystem to use the generated profiles, and is a standalone utility rather than an integrated calibration engine . **Best for Adobe users** wanting custom profiles for lenses not covered by Adobe's built-in database, accepting the Windows-only and Adobe-locked workflow.

- **DxO OpticsPro Lens Modules** — **The commercial lens correction standard.** DxO's proprietary modules provide per-lens, per-camera correction for distortion, vignetting, chromatic aberration, and sharpness. **Included with DxO PhotoLab licensing**. **Best for DxO users** wanting best-in-class automatic corrections, accepting the closed ecosystem and subscription/perpetual cost.

## Open-Source GitHub Projects

- **Lensfun** — **The open-source lens database and correction library that powers most open-source photography software.** **LGPL-3.0 licensed**, **lensfun 0.3.4** is the current stable release . **Provides an open database of photographic lenses and their characteristics**, with a library that reads and searches the database and applies correction algorithms . **Corrects distortion, transversal (lateral) chromatic aberration, vignetting, and color contribution** . **Used by darktable, RawTherapee, digiKam, and other open-source photo editors** as their correction engine. **Available via package managers** (Fedora, Debian, Arch) with tools, Python bindings, and development headers . **The honest caveat**: **it is a library, not a standalone application** — you need a photo editor that integrates it, and adding new lenses to the database requires calibration data and community contribution. **Best for open-source photography workflows** needing reliable, database-driven lens correction without proprietary dependencies.

- **Hugin Calibrate Lens GUI** — **The GUI-driven straight-line lens calibration tool.** **Free and open-source**, part of the Hugin panorama stitcher suite . **Uses the straight-line approach**: load images with straight lines (buildings, string, horizon), run Canny edge detection to find lines, then optimize lens parameters (a, b, c radial distortion coefficients) by minimizing how curved those lines appear . **Workflow**: load images → check focal length/crop factor from EXIF → detect lines → optimize lens parameters → save for use in Hugin . **Line detection is tunable** via scale/radius and threshold, with a preview showing edge detection and corrected results, and manual marking of bad lines to exclude them from optimization . **The honest caveat**: **requires images containing straight lines** — it is not a checkerboard-based calibration tool, and its primary output is Hugin-compatible parameters rather than a universal profile format. **Best for Hugin users and anyone needing a GUI-driven straight-line calibration** without writing scripts or using proprietary tools.

- **PTLens / clens** — **The classic automatic lens correction tool with a command-line counterpart.** **PTLens is a free add-on for Panorama Tools** that automatically corrects vignetting, pincushion distortion, and barrel distortion . **Available as a Photoshop plugin and standalone Windows program**, with **clens** — a command-line version using the same lens database — available for Linux, Windows, and OS X . **Supports a wide range of prosumer and SLR cameras**, and if your camera/lens combination is missing, you can forward calibration pictures to the author for inclusion . **The honest caveat**: **legacy tooling** — PTLens dates back to the mid-2000s, and while clens remains useful for scripted correction, the project is not actively developed as a modern calibration suite. **Best for batch/scripted correction** where a command-line tool with a known lens database fits the workflow.

- **gyroflow** — **The video stabilization tool with integrated lens calibration.** **Open-source, hardware-accelerated**, using gyroscope and accelerometer data for pixel-level stabilization . **Includes lens calibration capabilities**: determines focal length and lens distortions by analyzing calibration patterns to create a lens profile, and calculates intrinsic/extrinsic camera parameters to correct distortion . **Integrates with professional NLEs via plugins** so stabilization and correction can be applied directly to timelines . **The honest caveat**: **video-focused** — its calibration is in service of stabilization rather than stills photography, and the workflow is tuned for motion footage. **Best for videographers** needing lens distortion correction as part of a gyro-stabilization pipeline.

- **Kalibr** — **The robotics-grade multi-camera and visual-inertial calibration suite.** **Open-source (ETH Zurich)**, providing a mathematical framework for determining intrinsic and extrinsic parameters across multiple cameras and spatio-temporal offsets between cameras and IMUs . **Features a non-linear least-squares optimizer** minimizing reprojection and inertial errors, with specialized tools for **rolling-shutter camera calibration** . **The honest caveat**: **robotics/computer-vision focused** — it is not a photography lens-profile generator, and setup requires calibration targets and technical expertise. **Best for robotics and CV researchers** needing precise multi-sensor calibration, not for photographers creating `.lcp` profiles.

### Additional Strong Open-Source Options

- **lens-distortion-rectification (bbenligiray)** — **Blind radial distortion rectification by line straightness.** Matlab implementation, 28+ GitHub stars . **Corrects distortion without a calibration pattern** by exploiting straight lines in the scene. **Best for research and blind correction scenarios** where no calibration target is available.
- **opencv_live_distortion** — **Real-time OpenCV distortion correction with parameter tweaking.** Python-based, 5+ GitHub stars . **Best for interactive experimentation** with OpenCV's distortion models.

**Frameworks for building custom systems**: Combine **Lensfun** for database-driven correction inside a photo editor, **Hugin Calibrate Lens GUI** for generating custom correction parameters from straight-line scenes, **PTLens/clens** for scripted batch correction, and **gyroflow** for video stabilization with lens correction — to build a lens calibration and correction stack tailored to your need for stills profiles versus video stabilization, and database lookup versus custom calibration.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Lens calibration tools differ significantly in calibration method (checkerboard vs straight-line vs blind), output format (`.lcp` vs Lensfun database vs Hugin parameters), and integration ecosystem. **Adobe Lens Profile Creator is Windows-only freeware** that produces `.lcp` files usable only in Adobe software . **Lensfun is a library, not an application** — its correction capability depends on the photo editor that integrates it, and its database grows through community contribution . **Hugin's calibrate_lens_gui requires straight lines in the scene** and outputs Hugin-compatible parameters rather than universal profiles . **PTLens/clens is legacy tooling** — useful for scripted correction but not a modern calibration suite . **Kalibr is for robotics**, not photography . **The choice often comes down to output target**: `.lcp` for Adobe, Lensfun database for open-source editors, or Hugin parameters for panorama stitching.
- Self-hosted open-source solutions require proper library installation (Lensfun via package manager), calibration target acquisition or straight-line scene capture, and awareness that lens correction is most accurate when calibration is performed at the same focal length and focus distance as the intended shoot.

---

**Made for photographers, videographers, and computer-vision engineers choosing lens calibration tools that match their correction target and workflow.**
Let's make lens calibration more open, database-driven, and calibration-method-transparent.
