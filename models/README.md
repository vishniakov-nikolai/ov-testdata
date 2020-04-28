# Generate INT8 Models

To calibrate your model to the INT8 precision, follow the steps below:

1. Install the Accuracy Checker and Post-Training Optimization tool in your environment. Both tools
   are delivered as a part of the OpenVINO™ toolkit, but you can use the Accuracy Checker
   directly from the [Open Model Zoo GitHub*
   repository](https://github.com/opencv/open_model_zoo/tree/master/tools/accuracy_checker) if you
   like.

2. Download a dataset and convert annotations to the [Accuracy Checker friendly
   format](https://github.com/opencv/open_model_zoo/blob/master/tools/accuracy_checker/accuracy_checker/annotation_converters/README.md).

3. [Convert your model to the Intermediate Representation
   (IR)](https://docs.openvinotoolkit.org/latest/_docs_MO_DG_prepare_model_convert_model_Converting_Model.html).
   The IR contains a generated JSON config file for calibration. Find examples like
   [inception_v3.json](./inception_v3/inception_v3.json) in the directories of INT8 models. 

4. Run the Post-Training Optimization tool with the JSON config file and wait for the calibration
   process completion.
 