# TENSORFLOW LITE OBJECT DETECTION -  ASSIGNMENT


## OVERVIEW 
This project implements TensorFlow Lite object detection models for following real-world use cases:
PCB Fault Detection

The models detect objects in images and output bounding boxes, class labels, and confidence scores, optimized for edge and mobile deployment using TensorFlow Lite.

### Use Case : PCB Fault Detection

### Objective - Detect PCB manufacturing defects such as:

- Soldering defects
- Missing components
- Damaged components



## DATASET
Source: https://universe.roboflow.com/object-detection-dt-wzpc6/pcb-dataset-defect
- 219 manually selected and annotated images

### Annotation tool : Label Studio (open source) 
https://labelstud.io/

### Annotation format: Text (txt)

### Classes
- Hole
- Mouse bite
- Open circuit
- Short
- Spur
- Spurious


## TensorFlow Lite Conversion 
YOLOv8 to TensorFlow Lite Conversion :
This project uses YOLOv8 for object detection and converts the trained model into TensorFlow Lite (TFLite) format for deployment on edge and mobile devices.
Ultralytics provides native support for exporting YOLOv8 models to TFLite, making the conversion process straightforward.

```bash
  pip install ultralytics
  from ultralytics import YOLO
  model = YOLO("yolov8n.pt")
  model.export(format="tflite")
```

## Output
Each model outputs:

1. Bounding boxes
2. Class labels
3. Confidence scores


![train_batch2](https://github.com/user-attachments/assets/56ff77b6-57b1-4fdc-a7d5-1b2840005027)


![train_batch1](https://github.com/user-attachments/assets/eb2b129e-9aaf-4b91-912d-1086e9a0a0dc)



<img width="1920" height="1080" alt="Screenshot 2026-01-18 141322" src="https://github.com/user-attachments/assets/61deca69-43b8-4ed0-9a23-87ef8a9ca5eb" />


<img width="1920" height="1080" alt="Screenshot 2026-01-18 141559" src="https://github.com/user-attachments/assets/69dbc5eb-728a-4e56-b9a9-53e20890e94b" />


<img width="670" height="819" alt="Screenshot 2026-01-18 141746" src="https://github.com/user-attachments/assets/4dc296ef-c867-4bb5-9b3c-d667b6fee802" />



### Model files:
- my_model.pt
- my_model.tflite


## Known Limitations & Challenges 

- Limited dataset size may affect generalization
- Class imbalance in PCB defect types
- Performance sensitive to lighting and image quality
- Accuracy can be improved with more data and augmentation

## Future Improvements
- Increase dataset size
- Add data augmentation
- Use int8 quantization


## Conclusion

### This project demonstrates an end-to-end object detection pipeline:
- Data preparation
- Model training
- Optimization
- Deployment using TensorFlow Lite

The solution is suitable for embedded and mobile applications.
