# ucla_ajl_team_6

## Starter Notes for Image Processing Step

### Image Processing; Simple Classification
* Simple Classification:
  * binary (ex: image is a cat or dog)
  * can be multi-class (ex: makes or models of cars)
* Multi-label Classification:
  * algo is trained to recognize multiple aspects of an image

### A Persistent Challenge: Size Constraints
* Good images tend to be large
* However, runtime can take many hours
* Strategy?
  * Reshaping images to be smaller
  * Not immediate solution, but can work to get started

### Filter Out Bad Data
* Files can be corrupt
* Can filter out bad data by checking for the JFIF metadata flag to see if an image is a valid JPEG image

### EDA
* Useful to know the size (height, width) and channel values (Red, Green, Blue color levels) for the images

### Generate the Dataset
* Image data needs to be standardized for the ML algo
* Handled using built in Keras Utility
* standardizing the image data while using the image_dataset_from_directory function
  * Directory
    * path of the directory where the images are
  * Labels
    * tells us how to assign the labels
    * If set to inferred, the directory should contain subdirectories who's names are the class names
     * So Cat is 0 and Dog is 1 for example

### Aside: Another Big Challenge of Image Data
* Not enough images to build effectice model?
* Use "image data agmentation"
  * rotate, shape, or flip images we have to give our algorithm more data to look at
  * idea: could use this technique on darker skin tones to increase representation? or on skin issues that are not high in our dataset?

### Additional Preprocessing
* neural networks prefer smaller input values (color channels). So we can standardize the channels to the [0,1] range.
* If we have a GPU, we can built this feature into the model. If we just have a CPU, we can build it into the dataset

### Build the Model
* Notebook uses a smaller version of Xception network, which is a powerful image classification network built by Google.

### Tip for training
* If training takes too long or exhausts system resources, we can make the batch_size in the image_dataset_from_directory function smaller.
* This is said to be the fastest way to reduce the RAM requirements for trainning.

### Image Processing: Multi-Label Classification
* The next section of the notebook talks about multi-label classification, where there could be two things in an image that we are looking for, like a "man" and a "suit" in one image
* For now doing multi-class classification for out dataset is a good place to start, where we classify the different skin problems in the images since each image is just one skin issue.
* Will add more notes here later for multi-label classification if we decide to implement this into our model


