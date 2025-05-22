# Hand-Recognition

Identifies the presense of a hand in the frame and identifies the number of fingers being held up.

# Algorithm

SET                 Camera on
READ              Available frame
SET                  Frame as 1st one 
	           Region of interest
CONVERT       Change from BGR color scheme to hsv/black and white
DEFINE            Skin color range
MASK              Extract and mask skin color (Gaussian blur) 
FIND                All possible Contours; followed by ones of greatest area
MAKE              Convex hull around the hand; define area of hand
FIND                The defects in convex hull due to hand
                         Defects due to fingers 
	            Distance and angle between point and convex hull
DO                    Ignore angle>90 
                          Draw boundary around hand/ finger tips (whatever be the case)
                          Count number of fingers
PRINT               The number observed based on the mix match of hull area and nodes
CLOSE               Quit Camera when exit condition is met
![image](https://github.com/user-attachments/assets/4b594d90-05ec-492c-b47e-7264585400d6)
