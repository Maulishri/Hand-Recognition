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

# Sample Outputs

<img width="468" alt="image" src="https://github.com/user-attachments/assets/6fc43649-2bbd-4abe-b271-18b9ae5b48e9" />

<img width="468" alt="image" src="https://github.com/user-attachments/assets/79c25fe5-aed0-4ed8-a37e-1a5218f7ae0c" />

<img width="468" alt="image" src="https://github.com/user-attachments/assets/35444f8c-9e05-4031-8044-ac39a67f32ce" />




