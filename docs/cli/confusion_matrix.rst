.. _cli/confusion_matrix:

Confusion matrix comparing ground truth and predicted bounding boxes detected by a model
========================================================================================

Assuming you already have both your dataset and predicted output ready::

  $ lumi confusion_matrix --groundtruth_csv lumi_csv/val.csv --predicted_csv preds_val/objects.csv --output_txt outout_18.txt --classes_json all_data/classes.json

The ``lumi confusion_matrix`` CLI tool provides the following options related to training.

* ``--groundtruth_csv``: Absolute path to csv containing image_id,xmin,ymin,xmax,ymax,label and several rows corresponding to the groundtruth bounding box objects

* ``--predicted_csv``: Absolute path to csv containing image_id,xmin,ymin,xmax,ymax,label,prob and several rows corresponding to the predicted bounding box objects

* ``--output_txt``: Output txt file containing confusion matrix, precision, recall per class.

* ``--classes_json``: Path to a json file containing list of class label for the objects

* ``--iou_threshold``: IOU threshold below which the bounding box is invalid

* ``--confidence_threshold``: Confidence score threshold below which bounding box detection is of low confidence and is ignored while considering true positives