# Welding Defects Detector

#### Supported Labels
['Defect', 'Welding Line', 'Workpiece', 'porosity']

#### How to use
```
from ultralytics import YOLO

# Load a pretrained YOLO model
model = YOLO(r'weights\welding_defects_yolo11x.pt')

# Run inference on 'image.png' with arguments
model.predict(
    'image.png',
    save=True,
    device=0
    )
```
#### Confusion matrix normalized
![confusion_matrix_normalized.png](https://cdn-uploads.huggingface.co/production/uploads/62e1c9b42e4cab6e39dafc97/gflYDiDQL4P8ZUiij7Fnp.png)
#### Labels
![labels.jpg](https://cdn-uploads.huggingface.co/production/uploads/62e1c9b42e4cab6e39dafc97/0ZIgleo87QYeOBP4swPJj.jpeg)
![labels_correlogram.jpg](https://cdn-uploads.huggingface.co/production/uploads/62e1c9b42e4cab6e39dafc97/bHGE-LOjH4jgmbBShGZvC.jpeg)
#### Results
![results.png](https://cdn-uploads.huggingface.co/production/uploads/62e1c9b42e4cab6e39dafc97/83-tr_zbyudVR3EnRW6VU.png)
#### Predict
![val_batch0_labels.jpg](https://cdn-uploads.huggingface.co/production/uploads/62e1c9b42e4cab6e39dafc97/13x44dJn8_6rSgm7eEXRz.jpeg)
![val_batch0_pred.jpg](https://cdn-uploads.huggingface.co/production/uploads/62e1c9b42e4cab6e39dafc97/8luLKVm-7OSvwfkDXV27x.jpeg)
```
YOLO11x summary (fused): 464 layers, 56,831,644 parameters, 0 gradients, 194.4 GFLOPs
                 Class     Images  Instances      Box(P          R      mAP50  mAP50-95): 100%|██████████| 7/7 [00:06<00:00,  1.11it/s]
                   all        116        773      0.826      0.827      0.842      0.632
                Defect         56        131      0.552      0.427      0.445      0.202
          Welding Line        116        294      0.873      0.966      0.966      0.679
             Workpiece        110        307      0.941      0.987      0.992      0.938
              porosity         35         41      0.939      0.927      0.965       0.71
Speed: 0.5ms preprocess, 26.3ms inference, 0.0ms loss, 2.9ms postprocess per image
```

#### Others models...
https://huggingface.co/jparedesDS/
