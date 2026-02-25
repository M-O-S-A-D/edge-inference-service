# Edge Inference Service

## Overview
The Edge Inference Service is responsible for on-device AI processing within the Smart Surveillance System. It runs on embedded hardware such as NVIDIA Jetson Nano and Raspberry Pi.

This service performs real-time video analysis, face recognition, embedding generation, and activity detection before securely transmitting structured events to the cloud layer.

## Core Responsibilities
- Real-time video stream processing
- Face detection and recognition
- Vision-Language Model (VLM) inference
- Activity and object detection
- Feature embedding generation
- Local event tagging
- Privacy-preserving preprocessing

## Why This Service Exists
Sensitive biometric processing is performed locally to:
- Reduce cloud bandwidth usage
- Improve real-time responsiveness
- Preserve user privacy
- Enable offline fallback capabilities

The inference engine is isolated from networking logic to ensure hardware-specific optimizations (CUDA, TensorRT, ONNX) do not interfere with communication services.

## Technology Stack
- Python 3.8+
- PyTorch / TensorRT / ONNX Runtime
- OpenCV
- FAISS (optional local indexing)
- Docker support

## Deployment Target
- NVIDIA Jetson Nano
- Raspberry Pi
- Edge Linux environments

## Future Improvements
- Model versioning
- Edge caching improvements
- On-device anomaly detection
- Hardware acceleration tuning
