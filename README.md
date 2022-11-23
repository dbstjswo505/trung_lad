# Using the pupil location to detect the horizontal and vertical beatings. Real time pupil detection in noisy images

Finding pupil location inside the eye image is the prerequisite for eye tracking. A baseline is a hybrid model by inspiring YOLO, Network in Network and using Inception as the core CNN to predict the pupil location inside the image of the eye.

From the [repo](https://github.com/isohrab/Pupil-locator): To evaluate the model, the publicly available datasets [ExCuse, ElSe, PupilNet](http://www.ti.uni-tuebingen.de/Pupil-detection.1827.0.html) was used. The results surpass previous state of the art result (PuRe) by 9.2% and achieved 84.4%. The model's speed in an Intel CPU Core i7 7700 is 34 fps and in GPU gtx1070 is 124 fps. The images for training are noise free and the pupil is evident. The images are automatically labeled by [PuRe](https://arxiv.org/pdf/1712.08900.pdf) and the ground truth is the parameter of an ellipse.

### Run model
to predict the pupil location in a video, use this command:
```
python inferno.py PATH_TO_VIDEO_FILE

to run for beating detection, execute the below command:
# bash detect_beating.sh

```
### Acknowledgement 
This work was supported in part by the Institute for Information \& communications Technology Promotion (IITP) grant funded by the Korean government (MSIT) (No. 2021-0-01381, Development of Causal AI through Video Understanding) and was partly supported by the National Research Foundation of Korea (NRF) grant funded by the Korea government (MSIT) (No. 2022R1A2C201270611).

Code base for pupil locator was adopted from this [repo](https://github.com/isohrab/Pupil-locator).
