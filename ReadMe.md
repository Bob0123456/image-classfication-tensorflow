
#Image classification using Tensorflow

## Steps to run

1. Create a folder “flower_photos”

2. download flowers data 

``` http://download.tensorflow.org/example_images/flower_photos.tgz ```

3. Train flowers 

```
$python retrain.py --image_dir=flower_photos/ --output_graph=tf_files/retrained_graph.pb --output_labels=tf_files/retrained_labels.txt --bottleneck_dir=tf_files/bottlenecks/

```

4. Test model

```
$python label_image.py --image rose.jpg --graph=tf_files/retrained_graph.pb --labels=tf_files/retrained_labels.txt --input_layer=Placeholder --output_layer=final_result

```