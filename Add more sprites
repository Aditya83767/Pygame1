import math
import random
import pygame

pygame.init()
screen = pygame.display.set_mode((800, 500))
pygame.display.set_caption("Add more Sprites")
background = pygame.image.load("background.png")
playerImg = pygame.image.load("player.png")
enemyImg = pygame.image.load("enemy.png")
font = pygame.font.Font("freesansbold.ttf", 32)

# Player
playerX = 370
playerY = 380
playerX_change = 0
playerY_change = 0
score = 0

# TODO 1: make 7 enemies. Create num_of_enemies = 7 and two empty lists, enemyX and enemyY.
# Then use a for loop to add a random x (0 to 736) and a random y (50 to 400) for each enemy.


# TODO 2: write def isCollision(x1, y1, x2, y2) that returns True when the distance between
# the two sprites is less than 40. Use math.sqrt((x1 - x2) ** 2 + (y1 - y2) ** 2).


running = True
while running:
    screen.blit(background, (0, 0))

    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False
        # TODO 3: on KEYDOWN set playerX_change / playerY_change to -5 or 5 for the arrow keys.
        # On KEYUP set both changes back to 0.

    # TODO 4: add the changes to playerX and playerY, then keep the player inside the window.
    # (x from 0 to 736, y from 0 to 436)

    # TODO 5: loop over all the enemies. If the player collides with an enemy, add 1 to score and
    # move that enemy to a new random position. Then draw the enemy with screen.blit(enemyImg, (x, y)).

    screen.blit(playerImg, (playerX, playerY))
    screen.blit(font.render("Score : " + str(score), True, (255, 255, 255)), (10, 10))
    pygame.display.update()
