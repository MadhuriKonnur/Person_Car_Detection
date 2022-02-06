# Person_Car_Detection
Using FiftyOne App
Link to download the dataset: https://evp-ml-data.s3.us-east-2.amazonaws.com/ml-interview/openimages-personcar/trainval.tar.gz

Annotation format:COCO

Using the open-source machine learning developer tool, FiftyOne, to easily work with and visualize image and video datasets with annotations and model predictions

Challenge: Since we have custom data in COCO format .Which was not available on fiftyone zoo library. Hence  used add_coco_labels() to conveniently add the labels to an existing dataset.

Det_mk_EV.ipynb includes:
1.round-trip export and then re-import of both images-and-labels and labels-only data in COCO format
2. Model building  and  training using "ssd-mobilenet-v1-fpn-coco-tf " from available zoo lib
3. FPN Single Shot Detector model from SSD: Single Shot MultiBox Detector-supports detection,coco,tf with MobileNetV1 backbone trained on COCO.
4. outcome of training:
5.  mAP:0.367
6.  person AP:0.342
7.  car AP:0.208

  List of Evaluation run  on dataset sample
  {
    "key": "eval",
    "version": "0.14.3",
    "timestamp": "2022-02-06T18:28:26.881000",
    "config": {
        "method": "coco",
        "cls": "fiftyone.utils.eval.coco.COCOEvaluationConfig",
        "pred_field": "predictions",
        "gt_field": "ground_truth",
        "iou": 0.5,
        "classwise": true,
        "iscrowd": "iscrowd",
        "use_masks": false,
        "use_boxes": false,
        "tolerance": null,
        "compute_mAP": true,
        "iou_threshs": [
            0.5,
            0.55,
            0.6,
            0.65,
            0.7,
            0.75,
            0.8,
            0.85,
            0.9,
            0.95
        ],
        "max_preds": 100,
        "error_level": 1
    }
}
9. 
