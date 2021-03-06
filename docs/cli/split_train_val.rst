.. _cli/split_train_val:

Split a dataset into training and validation
============================================

Assuming you already have both your dataset and their bounding box, labeled annotations ready::

  $ lumi split_train_val bb_labels_no_mosaic.txt --output_dir all_data_no_mosaic_lumi_csv --percentage 0.8 --random_seed 42 --filter_dense_anns True --input_image_format .tif

The ``lumi split_train_val`` CLI tool provides the following options related to splitting and organizing the data.

* ``filenames``: List of all the bounding box annotation files, can be 1 to n, can be text or csv files

* ``--percentage``: Percentage of total images to add to the train directory, 1 - percentage is added to the val directory, defaults to 0.8

* ``--random_seed``: Random seed for shuffling the images, defaults to 43

* ``--filter_dense_anns``: If this flag is set to True, images with class that has more annotations are completely ignored, this flag defaults to false

* ``--input_image_format``: Format of images in input directory
