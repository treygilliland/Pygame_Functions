# Pygame Functions

## To use:

1. Place the pygame_functions.py file in the same directory as your main .py file.

2. Write this command at the top of your main .py file
```
from pygame_functions import *
```

>Note:
This import initializes both pygame and pygame.mixer for use in your game.  

3. Finally, use the screenSize() function to create a screen object for your game.

```
screenSize(SCREEN_WIDTH, SCREEN_HEIGHT)
```

You can now use any class, functions, variables included in this wrapper :)  

See below for an overview of included variables, classes, and functions.

## What pygame_functions.py provides:
### Global Variables
> Note: These variables are mostly manipulated using related functions (see below) but can be manipulated directly.

spriteGroup - manage sprite objects here  
textboxGroup - manage textbox objects here  
hiddenSprites - manage hidden sprites here  

gameClock - clock instance  
screen - screen instance  
background - background instance  

musicPaused - flag for pausing music  
screenRefresh - flag for enabling screen refresh  

keydict - maps key strings to pygame key representation
> ex: "space" == pygame.K_SPACE

### Classes (signatures)

Background()

newSprite(filename, frames)  
newTextBox(text, xpos, ypos, width, case, maxLength, fontSize)  
newLabel(text, fontSize, font, fontColour, xpos, ypos, background)

### Functions

System:
>	loadImage(fileName, useColorKey=False)  
	makeImage(filename) (Note: same as loadImage)  
	screenSize(sizex, sizey, xpos=None, ypos=None, fullscreen=False)  
	pause(milliseconds, allowEsc=True)  
	end()  
	endWait()  
	clock()  
	tick(fps)  
	updateDisplay()  
	parseColour(colour)  
	setAutoUpdate(val)  

Background:  
>	setBackgroundColour(colour)  
	setBackgroundImage(img)  
	scrollBackground(x, y)  

Sprites  
>	moveSprite(sprite, x, y, centre=False)  
	rotateSprite(sprite, angle)  
	transformSprite(sprite, angle, scale, hflip=False, vflip=False)  
	killSprite(sprite)  
	hideSprite(sprite)  
	hideAll()  
	unhideAll()  
	showSprite(sprite)  
	makeSprite(filename, frames=1)  
	addSpriteImage(sprite, image)  
	changeSpriteImage(sprite, index)  
	nextSpriteImage(sprite)  
	prevSpriteImage(sprite)  
	touching(sprite1, sprite2)  
	allTouching(spritename)  

Shapes  
>	drawRect(xpos, ypos, width, height, colour, linewidth=0)  
	drawLine(x1, y1, x2, y2, colour, linewidth=1)  
	drawPolygon(pointlist, colour, linewidth=0)  
	drawEllipse(centreX, centreY, width, height, colour, linewidth=0)  
	drawTriangle(x1, y1, x2, y2, x3, y3, colour, linewidth=0)  
	clearShapes()  
	updateShapes()  

Sounds  
>	makeSound(filename)  
	playSound(sound, loops=0)  
	stopSound(sound)  
	playSoundAndWait(sound)  
	makeMusic(filename)  
	playMusic(loops=0)  
	stopMusic()  
	pauseMusic()  
	rewindMusic()  

Text  
>	makeLabel(text, fontSize, xpos, ypos, fontColour='black', font='Arial', background="clear")  
	moveLabel(sprite, x, y)  
	changeLabel(textObject, newText, fontColour=None, background=None)  
	showLabel(labelName)  
	hideLabel(labelName)  
	makeTextBox(xpos, ypos, width, case=0, startingText="Please type here", maxLength=0, fontSize=22)  
	textBoxInput(textbox, functionToCall=None, args=[])  
	showTextBox(textBoxName)  
	hideTextBox(textBoxName)  

Mouse & Keyboard  
>	waitPress()  
	keyPressed(keyCheck="")  
	mousePressed()  
	spriteClicked(sprite)  
	mouseX()  
	mouseY()  
