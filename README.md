# voc2coco

This is script for converting VOC format XMLs to COCO format json(ex. coco_eval.json).

### Why we need to convert VOC xmls to COCO format json ?

We can use COCO API, this is very useful(ex. calculating mAP).

## NOTE:

This script is only expecting Pascal VOC files which are created by MS VoTT.

### 2. Run script

##### 2.1 Usage 1(Use ids list)

```bash
$ python voc2coco.py \
    --ann_dir /path/to/annotation/dir \
    --ann_ids /path/to/annotations/ids/list.txt \
    --labels /path/to/labels.txt \
    --output /path/to/output.json \
    <option> --ext xml
```

### 3. Example of usage

```bash
$ python voc2coco.py --ann_dir bush_voc/Annotations --ann_ids bush_voc/ImageSets/Main/clinch_train.txt --labels bush_voc/pascal_label_map.pbtxt --output bush_coco/bccd_test_cocoformat.json --ext xml
```

### REFERENCES:

- https://github.com/anhlt/faster_rcnn/tree/e60becf4d46856421e681268a06bca7f0dcee699/faster_rcnn/utils/datasets/voc
