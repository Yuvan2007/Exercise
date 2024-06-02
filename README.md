import cv2
import numpy as np

img = cv2.imread('C:/Users/91720/Downloads/daylight-environment-forest-459225.png')
cv2.imshow("Image",img)
cv2.waitKey(0)


#gray_image = /img{Grayscale} = 0.2989 /cdot /img{Red} + 0.5870 /cdot /img{Green} + 0.1140 /cdot /img{Blue} 
g_image = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)

cv2.imshow("",g_image)
cv2.waitKey(0)
cv2.destroyAllWindows()
