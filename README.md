# 






import pygame, random, sys
from pygame.locals import *

pygame.init()
fpsClock = pygame.time.Clock()
surface = pygame.display.set_mode((800, 600))
surface.fill((0, 0, 0))
start = (random.random() * 800, random.random() * 600)

while True:
   for event in pygame.event.get():
       if event.type == QUIT:
           pygame.quit()
           sys.exit()
   end = (random.random() * 800, random.random() * 600)
   color = (random.random() * 255, random.random() * 255, random.random() * 255)
   pygame.draw.line(surface, color, start, end)
   start = end
   pygame.display.update()
   fpsClock.tick(60)
