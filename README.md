# Human Detection with YOLO

An archive of YOLOv5, YOLOv7, and YOLOv8 experiments, including custom postprocessing scripts and an input/output video pair.

[Input clip](assets/example-input.mp4) · [Output clip](assets/example-output.mp4) · [Original report](docs/report.pdf)

## Organization

- `YOLOv5/` and `YOLOv7/`: selected upstream training/inference scripts retained with their source notices.
- `YOLOv8/`: experiments around Ultralytics inference and custom postprocessing.
- `assets/`: short historical example clips.
- `docs/`: the original project report.

## Run and reproduce

These are selected experiment files, not complete vendored YOLO repositories. For v5/v7, use the matching upstream project and version described by its source headers; their full dependency trees are not included. For v8, install compatible `ultralytics` and `opencv-python` versions and review the selected script before running it.

The v8 video scripts accept `HUMAN_DETECTION_VIDEO` for the input and `HUMAN_DETECTION_MODEL` for the model path. Example, from `YOLOv8/`:

```sh
HUMAN_DETECTION_VIDEO=../assets/example-input.mp4 HUMAN_DETECTION_MODEL=yolov8s.pt python customyolo.py
```

Download the matching weights from the upstream model provider; generated checkpoints and output videos are ignored. Model labels and postprocessing must match the chosen weights. The example output illustrates an old run, not a current accuracy or speed benchmark.

## Credits

The YOLO implementations and pretrained models are upstream work. This archive preserves experiment scripts and postprocessing around them. Read the original report for the project context and keep upstream license notices when reusing code.
