# Pygame Functions

Originally created by StevePaget. 

Check out the wiki at https://github.com/StevePaget/Pygame_Functions/wiki

See video tutorials at https://www.youtube.com/playlist?list=PLeOSHd3t9lzKr4O3A3Q7OZyf8QwyCALyn


## To use  

Write this command at the top of your main .py file
```
from pygame_functions import *
```

Note  
This import initializes both pygame and pygame.mixer for use in your game.

## What Pygame Funcitons provides  
### Variables
spriteGroup - manage sprite objects here

textboxGroup - manage textbox objects here

hiddenSprites - manage hidden sprites here

gameClock - Clock instance

musicPaused - flag for pausing music

background??? -

screenRefresh??? - flag for enabling screen refresh

screen??? - 

keydict - maps key string to pygame enum representation
ex   "space" == pygame.K_SPACE

### Classes

Background() 

	setTiles(tiles) - takes in a path to tiles and adds variables to object

	scroll(x, y)

	setcolor(color) - sets background color


newSprite(filename, frames) (extends pygame.sprite.Sprite)

newTextBox(text, xpos, ypos, width, case, maxLength, fontSize) (extends pygame.sprite.Sprite)

newLabel(text, fontSize, font, fontcolor, xpos, ypos, background)

### Functions

System  
	loadImage(fileName, useColorKey=False)  
		- makeImage(filename)  
	screenSize(sizex, sizey, xpos=None, ypos=None, fullscreen=False)  
	pause(milliseconds, allowEsc=True)  
	end()  
	endWait()  
	clock()  
	tick(fps)  
	updateDisplay()  
	parsecolor(color)  
	setAutoUpdate(val)  

Background  
	setBackgroundcolor(color)  
	setBackgroundImage(img)  
	scrollBackground(x, y)  

Sprites  
	moveSprite(sprite, x, y, centre=False)  
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
	drawRect(xpos, ypos, width, height, color, linewidth=0)  
	drawLine(x1, y1, x2, y2, color, linewidth=1)  
	drawPolygon(pointlist, color, linewidth=0)  
	drawEllipse(centreX, centreY, width, height, color, linewidth=0)  
	drawTriangle(x1, y1, x2, y2, x3, y3, color, linewidth=0)  
	clearShapes()  
	updateShapes()  

Sounds  
	makeSound(filename)  
	playSound(sound, loops=0)  
	stopSound(sound)  
	playSoundAndWait(sound)  
	makeMusic(filename)  
	playMusic(loops=0)  
	stopMusic()  
	pauseMusic()  
	rewindMusic()  

Text  
	makeLabel(text, fontSize, xpos, ypos, fontcolor='black', font='Arial', background="clear")  
	moveLabel(sprite, x, y)  
	changeLabel(textObject, newText, fontcolor=None, background=None)  
	showLabel(labelName)  
	hideLabel(labelName)  
	makeTextBox(xpos, ypos, width, case=0, startingText="Please type here", maxLength=0, fontSize=22)  
	textBoxInput(textbox, functionToCall=None, args=[])  
	showTextBox(textBoxName)  
	hideTextBox(textBoxName)  

Mouse & Keyboard  
	waitPress()  
	keyPressed(keyCheck="")  
	mousePressed()  
	spriteClicked(sprite)  
	mouseX()  
	mouseY()  
