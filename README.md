# Amazon Rekognition Emotion Detection With Face Covered
This project is a simple demonstration of how to test the ability of Amazon Rekognition to identify emotions on faces with covering. It uses [Amazon Rekognition Face Detection](https://docs.aws.amazon.com/rekognition/latest/dg/faces-detect-images.html) to detect emotions in face images.   

There are two main focuses of this project: 
1. compare the emotion detection results of images without cover, with mask, and with sunglasses
2. compare the accuracy of emotion detection between humans and the machine 

***
## Choice of images
Each image used should has 3 versions: 
- The original face image, as the control group, should only has one person who faces front to the camera without covering on his face (glasses that are transparent are allowed because they will not cover the eyes), and the emotion on the face should be apparant enough to be identifies by both humans and the machine. 
- The image with mask should be the original image plus a face mask added using photo editing. 
- The image with sunglasses should be the original image plus sunglasses (black sunglasses to cover the eyes) added using photo editing. 


