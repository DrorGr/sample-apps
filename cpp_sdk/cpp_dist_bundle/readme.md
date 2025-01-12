# Trueface SDK

## Overview
The Trueface sdk library, dependency libraries, and header files `tf_sdk.h` and `tf_data_types.h` can be found in `./trueface_sdk/`.

## C++ Sample Code
Navigate to `c++/` and consult the readme file for build instructions.
The sample code demonstrates the basic functionality of the SDK, and provides a `CMakeLists.txt` file demonstrating how to compile and link against the SDK.
To explore full functionality, please consult the header files and the documentation.

## Model Files
The sample apps require certain models files to be downloaded (they will throw an exception if the model file is not detected).
The model files can be downloaded by running `./download_models/download_all_models.sh`. You can alternatively run individual scripts in that directory to download only the models you require. 
If you download the model files to a directory other than the build directory, you must specify the path to the directory using the `Trueface::ConfigurationOptions.modelsPath` configuration option.

## Documentation
The C++ SDK documentation can be found [here](https://reference.trueface.ai/cpp/master/latest/index.html), while the python bindings documentation can be found [here](https://reference.trueface.ai/cpp/master/latest/py/index.html)

## Sample Apps
Sample apps using the C++ SDK can be found [here](https://github.com/getchui/sample-apps). 
These sample apps extend the scope of the sample code and demonstrate more complete applications such as real-time streaming and video decoding apps.

## Benchmarks
To run speed benchmarks, navigate to `benchmarks/` and consult the readme file.
You can find our benchmarks [here](https://docs.trueface.ai/benchmarks).

## Minimum & Recommended Hardware Requirements
Minimum and recommended hardware requirements can be found here [here](https://docs.trueface.ai/minimum-recommended-hardware-requirements).

## ROC Curves
ROC curves are useful when choosing an operating threshold for face recognition applications. You can find the ROC curves [here](https://docs.trueface.ai/roc-curves).

## FAQ
A list of frequently asked questions with answers can be found [here](https://reference.trueface.ai/cpp/master/latest/faq.html)

## Running Sample Code from Github Repo
This sample code comes shipped as part of the SDK download bundle. 
If you are instead running this sample code by cloning the Trueface sample apps github repo [here](https://github.com/getchui/sample-apps), you will need to make a few modifications to get things working:

* Place the Trueface libraries in `./trueface_sdk/libs` and the Trueface header files in `./trueface_sdk/include`.
* Obtain the scripts for downloading the model files from the SDK download bundle.
