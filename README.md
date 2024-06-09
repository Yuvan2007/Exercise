#Importing 
import cv2
import numpy as np

#Reading and showing image  
img = cv2.imread("C:/Users/91720/Pictures/Saved Pictures/R.png")
cv2.imshow("Image",img)
cv2.waitKey(0)

#Creating and converting image matrix 
image_matrix = np.array(img)
image_matrix=cv2.resize(image_matrix,(480,240))
length = len(image_matrix)
width = len(image_matrix[0])
Gray_matrix = np.zeros((length,width))

for i in range(len(image_matrix)):
    for j in range(len(image_matrix[i])):
        pixel = image_matrix[i][j]
        (Blue, Green, Red) = image_matrix[i][j]
        Gray_matrix[i][j]=(Red+Green+Blue) *0.33
        #print(Gray_matrix[i][j])
        
print(Gray_matrix)
cv2.imshow("Gray_image",Gray_matrix)
cv2.waitKey(0)
