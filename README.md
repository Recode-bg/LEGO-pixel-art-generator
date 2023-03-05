# LEGO-pixel-art-generator
Python script to convert any image into a custom sized pixel-art version, where the pixels are equivalent to LEGO 1x1 blocks, and colours are matched to the nearest available lego colour. The script gives you a colour map and a block count by colour, which you can the order.

## Directory contents:
1) <b>colors.csv</b>: The dataset of lego colours. Includes the ID of the colour (acording to Lego's notation), That is what you would you would use to order something in that colour. Colours also have names (in the respective column). Then there is a column for the colour value in hex RGB, and finally a boolean value to denote if the lego items in this colour are transparent or solid.
2) <b>Lego Pixel Art Generator v.2.ipynb</b>: This is the latest version of the script (in an Jupyter notebook format). Scrol down for info on how to use.
3) <b>lego pixels.pdf</b>: This is the result of the script. Yoiu can use the resulting pdf as a guide to help you construct the image (once you have all the necessary bricks), and you can also use the table at the bottom of the page as a shopping list. The table tells you how many 1x1 Lego bricks of each colour (lego reference ID) you need.

## Usage guide:
If you have <a href="https://jupyter.org/">Jupyter notebook</a>, just download the notebook file and run it. If you don't, you can recreate it (use copy/paste :) in <a href="https://colab.research.google.com/">google colab</a>. Once you have it running, there is only two things that you have to supply as input. First you would probably want to you your own image, and second, you would probably want to define a custom size for the Lego "painting". Here is how to do that:
1) Custom file:
Find the 8th cell, where the code says: <code>image = Image.open('Mou-Aysha-portrait-photography-3.jpg')</code> and replace the image filename with yours. Mind that it expects the file to be in the same place as the script if you are only going to supply a filename. Otherwise, you will have to paste in the whole path to the file.
2) Custom poster size:
The size for the poster is defined in cell 10, where the code is <code>painting_base_size = int(input('Enter base size for the painting in mm. Value must be an integer: '))</code>. Wthen you execute that cell you will be given an input field to enter an <b>integer</b> in <b>milimeters!</b>. After that the script will calculate the exact size. It might be a little different from what you want, as a Lego 1x1 brick is 7.8 x 7.8 mm. Thus, any size you want will have to be divisible by 7.8 :D. For example the 300 mm I have last used as an example will actually become a painting of base size 296.4 mm. The height is driven by the ratio of the image you provided (you only choose the base/horizontal size).

Enjoy.
Alex