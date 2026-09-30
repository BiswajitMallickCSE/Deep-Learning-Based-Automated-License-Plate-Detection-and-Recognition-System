# 🚘 Deep Learning-Based Automated License Plate Detection and Recognition System

An automated License Plate Detection and Recognition system based on Deep Learning, Computer Vision, and Optical Character Recognition (OCR).

The system is designed to automatically detect vehicle license plates from images, extract the plate regions, recognize alphanumeric characters, and display the detected license plate numbers on the original image.

The current implementation supports detecting multiple license plates in a single image and applying OCR independently to each detected plate.

---

## 📌 Project Overview

Automatic License Plate Recognition (ALPR) is an important computer vision application used in intelligent transportation systems, parking management, traffic monitoring, vehicle access control, and security applications.

This project develops an end-to-end pipeline that combines:

- YOLO-based license plate detection
- OpenCV-based image preprocessing
- EasyOCR-based text recognition
- Tesseract OCR as a second OCR engine
- Multiple image preprocessing techniques
- OCR candidate voting and validation
- Multi-vehicle / multi-plate detection
- Automatic visualization of detected plates

The objective is to create a practical and extensible system capable of detecting and recognizing license plates from vehicle images.

---

## 🎯 Objectives

The main objectives of this project are:

1. Detect vehicle license plates automatically from input images.
2. Detect multiple license plates when multiple vehicles are present.
3. Extract individual license plate regions from the image.
4. Enhance plate images before OCR processing.
5. Recognize alphanumeric characters from license plates.
6. Combine multiple OCR results to reduce recognition errors.
7. Display detected plate numbers together with bounding boxes.
8. Save the final annotated output image.
9. Provide a foundation for future real-time video and traffic-monitoring applications.

---

## 🚀 Key Features

### 🔍 License Plate Detection

A dedicated YOLO-based license plate detection model is used to localize license plates in vehicle images.

### 🚗 Multiple Vehicle / Multiple Plate Detection

The system does not limit the processing to a single vehicle.

If an image contains multiple vehicles, the detector attempts to identify all visible license plates.

### 🔤 OCR-Based Recognition

The detected plate regions are processed using:

- EasyOCR
- Tesseract OCR

Using more than one OCR engine provides multiple recognition candidates.

### 🖼️ Image Preprocessing

Several preprocessing techniques are applied to improve OCR performance:

- Grayscale conversion
- Image upscaling
- Bilateral filtering
- CLAHE contrast enhancement
- Image sharpening
- Otsu thresholding
- Adaptive thresholding

### 🧠 OCR Candidate Voting

Instead of depending on a single OCR prediction, multiple OCR results from different preprocessing variants and OCR configurations are collected.Candidate plate strings are then ranked using a voting/score-based approach.

