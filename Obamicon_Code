from PIL import Image

# RGB values for recoloring.
darkBlue = (0, 51, 76)
red = (217, 26, 33)
lightBlue = (112, 150, 158)
yellow = (252, 227, 166)

# Import image.
my_image = Image.open("Basketball.png") #change IMAGENAME to the path on your computer to the image you're using
image_list = my_image.getdata() #each pixel is represented in the form (red value, green value, blue value, transparency). You don't need the fourth value.
image_list = list(image_list) #Turns the sequence above into a list. The list can be iterated through in a loop.

recolored = [] #list that will hold the pixel data for the new image.

#YOUR CODE to loop through the original list of pixels and build a new list based on intensity should go here.
for pixel in image_list :
    numRed = pixel[0]
    numBlue = pixel[1]
    numGreen = pixel[2]
    Sum = numRed+numBlue+numGreen
    if Sum<182:
        #color = (0, 51, 76)
        recolored.append(darkBlue)
    elif 182<Sum<364:
        #color = (217, 26, 33)
        recolored.append(red)
    elif 364<Sum<546:
        #color = (112, 150, 158)
        recolored.append(lightBlue)
    else:
        #color = (252, 227, 166)
        recolored.append(yellow)

# Create a new image using the recolored list. Display and save the image.
new_image = Image.new("RGB", my_image.size) #Creates a new image that will be the same size as the original image.
new_image.putdata(recolored) #Adds the data from the recolored list to the image.
new_image.show() #show the new image on the screen
new_image.save("recolored.png", "png") #save the new image as "recolored.jpg"
