import pygame, sys
from pygame.math import Vector2
#definitions and game window
pygame.init() #initiating pygame

GREEN = (173, 204, 96) #RGB colorcodes
DARK_GREEN = (43, 51, 24)

cell_size = 30
number_of_cells = 25

class Food():
    def __init__(self):#initialises object
        self.position = Vector2(5,6) #vector2 position that holds the position of the object in cells.

    def draw(self, screen):  # Passing screen as argument
        food_rect = pygame.Rect(self.position.x * cell_size, self.position.y * cell_size, cell_size, cell_size)
        screen.blit(food_surface, food_rect)  # Corrected typo


screen = pygame.display.set_mode((cell_size*number_of_cells, cell_size*number_of_cells)) #this is the width, heigt of the display --> game window

pygame.display.set_caption("Snake Game") 

clock = pygame.time.Clock() #to control how fast the game runs --> getting back to this later

food_surface = pygame.image.load("Python/png-transparent-star-golden-stars-angle-3d-computer-graphics-symmetry-thumbnail.png")
food = Food()
#this is the game loop
while True:
    for event in pygame.event.get(): #list of events recognised by pygame
        if event.type == pygame.QUIT:
            pygame.quit()
            sys.exit()
    
    #Drawing
    screen.fill(GREEN)    
    food.draw(screen)
    
    pygame.display.update()
    clock.tick(60) #the while loop will run 60 times per second (without this, the game runs as fast as the computer can handle)
