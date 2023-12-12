# Tema1 from Programming course, solved by Vlada Pulbere, 312 CB
This homework includes solving 6 tasks, that require writing 6 different functions that process given images.
## Task 1 - Horizontal Flip 
The main goal of this task is to implement a function that flips (or a mirrors) a given image. 
The function takes an image represented as a 3D array (int ***image), where N is the number of rows, M is the number of columns, and a third dimension that represents the color of the pixel. The output of the function (***filp_horizontal) is returning the image obtained by mirroring the input image. The algorithm used is iterating through each row of the image and through each column up to half of the given columns, because by swapping values of every element, when the contor will get to the middle of the matrix (vertically), it will have every value already swapped. The constant mirror ( = M - 1 - j) calculates the mirror index for the current column. This index corresponds to the column on the opposite side of the row. The next loop iterates through the rgb values and swaps the color values between the current column and the mirror column.

## Task 2 - Rotate Left
This function rotates the given image 90 degrees in a counter clockwise way and stores the rotated image in a new allocated 3D array. The overall logic of the algorithm is copying the pixel values ( Red Green and Blue channels) from the original image to the rotated image, for each row and column, by finding the new position of the column in a row-wise way. Then the function has a part of deallocating the memory used by the original image to prevent memory leaks.

## Task 3 - Crop
The Crop function generally creates a new image by extracting a rectangular region from the original image.
This function starts by allocating memory for the cropped image (crop_img).  Next, the function copies each of the pixel values (Red Green and Blue) from the specified region of the original image to the corresponding positions in the cropped image (crop_img), based on the input parameters x, y, h, and w.
The function returns the pointer to the cropped image.

Then, by implementing a if-statement, I'm checking whether the current pixel should take the color values from the original image or should be filled with new color values - by determining if the current position of the pixel is outside the region specified by the parameters rows and cols or not.
