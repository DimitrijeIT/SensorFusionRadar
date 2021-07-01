
## Implementation steps for the 2D CFAR process.

Move the window over the complete matrix (keeping in mind to start and end with enough cells to calculate threshold noise)
For each CUT, calculate the average noise level in surrounding training cells.  
If the CUT signal is higher than noise level + offset then set the output to 1. If the signal is below the noise threshold set it to 0. 

## Selection of Training, Guard cells, and offset.
Tr = 14, Td = 7. A little bit more cells are used than initially proposed to have a better average. 
Gr = 6, Gd = 3
Offset = 6. This offset gave the best result during the testing phase. 

## Steps taken to suppress the non-thresholded cells at the edges.
The output of cfar signal is set to 0 for the rows from 1 to Tr+Gr and the same amount from the end 
The output of cfar signal is set to 0 for the columns from1 to Td+Gd and the same amount from the end 

![image](https://user-images.githubusercontent.com/25511928/124161010-2f1bbe00-da9d-11eb-95f1-e0c1614ff9de.png)

![image](https://user-images.githubusercontent.com/25511928/124161021-33e07200-da9d-11eb-909f-582b59e2cbf1.png)

![image](https://user-images.githubusercontent.com/25511928/124161030-3773f900-da9d-11eb-80cb-142fdca6726b.png)






