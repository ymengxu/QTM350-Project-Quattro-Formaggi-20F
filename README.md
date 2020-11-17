# Amazon Rekognition Emotion Detection With Face Covered
This project is a simple demonstration of how to test the ability of Amazon Rekognition to identify emotions on faces with covering. It uses [Amazon Rekognition Face Detection](https://docs.aws.amazon.com/rekognition/latest/dg/faces-detect-images.html) to detect emotions in face images.   

There are two main focuses of this project: 
1. compare the emotion detection results of images without cover, with mask, and with sunglasses
2. compare the accuracy of emotion detection between humans and the machine 

***
## Choice of images
Each image used should have 3 versions: 
- The original face image, as the control group, should only have one person who is facing front to the camera without covering on his face (glasses that are transparent are allowed because they will not cover the eyes), and the emotion on the face should be apparant enough to be identified by both humans and the machine. 
- The image with mask should be the original image plus a face mask added using photo editing. 
- The image with sunglasses should be the original image plus sunglasses (black sunglasses to cover the eyes) added using photo editing.    

Gather as many images as possible for each emotion among **HAPPY | SAD | ANGRY | CONFUSED | DISGUSTED | SURPRISED | CALM | FEAR**, which are the valid values for Rekognition emotions identification. 

***
## Compare images without cover, with mask, and with sunglasses
To start, create a notebook on Amazon SageMaker. Store every image in an S3 bucket so that they can be called by Rekognition in the notebook. Test each image using Amazon Rekogtion Face Detection and record the list of emotions and their confidence levels.   
The example result should be like this:    
![Example result](https://raw.githubusercontent.com/ymengxu/QTM350-Project-Quattro-Formaggi-20F/main/readme%20picture/5.PNG)  
To compare images of one emotion without cover, with mask, and with sunglasses, draw a boxplot or violinplot with the 3 types (no cover, mask, sunglasses) on the x axis, and the confidence level of that emotion on the y axis. To produce more credible result, you need a fair amount of images of each emotion.  
You can also compare between emotions to investigate if Rekognition identify some emotions better than others when the image is covered with mask or sunglasses by comparing the plot of each emotion. Since there are not enough images for every emotion, this step is not demonstrated in the project.   
Focusing on the top emotion guess of each image is also a potential area. You can investigate what is the most commonly identified emotion among images with mask and among images with sunglasses.

***
## Compare between humans and the machine
First, gather information of how people detect emotions in the same images you use Rekognition to test. You can gather information by a survey using google forms. The survey should contain multiple choice questions, each showing an image, and asks the respondents to choose the emotion they think the person in each image is expressing. The choices for each question are HAPPY | SAD | ANGRY | CONFUSED | DISGUSTED | SURPRISED | CALM | FEAR. Note that you should not include images with no cover in the survey and remember to randomly shuffle the images. 


