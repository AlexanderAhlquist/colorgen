# colorgen

#In this document I am going to try to create a system in which three random numbers are generated in order to randomly generate a color which can exist on a color hex. This is just a conceptual part of an idea and a way for me to practice coding.

import random

Generate = "Ready"


def colorgen():
	red = random.randint(0, 255)
	green = random.randint(0, 255)
	blue = random.randint(0, 255)
	print()
	print("This is the RGB value of your color!")
	print((red, green, blue))
	print()
	print("This is the hex-code of your color!")
	print('#%02X%02X%02X' % (red, green, blue))
	print()
	print(
	    "I hope you love your color! Here's a link to it so you can see what it looks like!"
	)
	print()
	print("http://www.color-hex.com/color/"
	      '%02X%02X%02X' % (red, green, blue))
	print()


while Generate == "Ready":
	print("----------------------------")
	print()
	Generate = input("Would you like to generate a brand new color? y/n:")
	if Generate == "y":
		colorgen()
		Generate = "Ready"
	if Generate == "n":
		print()
		print("Sorry, that's all I can do!")
		print()
		Generate = "Ready"

