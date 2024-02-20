import pygame, random, sys

pygame.init()

#display
dis=pygame.display.set_mode((600,500))
pygame.display.set_caption("Python's Pit")

pink = (255,100,180)
purple = (240,0,255)
blue_green = ((0,255,170))
black = (0,0,0)
white = (255,255,255)

dis.fill(black)
game_over= False
game_close = False
x = 300 
y = 200 
x_change = 0
y_change = 0 


score = 0 
clock=pygame.time.Clock()
font_style=pygame.font.SysFont("freesans", 25)


def wrap_position():
    global x, y 
    if x >= 600:
        x = 0 
    elif x < 0:
        x = 590 
    elif y >= 500:
        y = 0
    elif y < 0:
        y = 490



def game_loop():
    game_over=False
    game_exit = False
    x=300 
    y=200 
    x_change=0
    y_change=0
    foodx= 10*random.randint(0,59)
    foody= 10*random.randint(0,39)
    while(game_close==False):
            while(game_close==True):
                dis.fill(black)
                dis.blit( [100.100])
                pygame.display.update()
                for event in pygame.event.get():
                    if event.type == pygame.QUIT:
                        game_over = True
                        game_close = False
                    if event.type == pygame.KEYDOWN:
                        if event.key==pygame.K_q:
                            game_over=True
                            game_close=False
                        if event.key==pygame.K.q:
                            game_loop()
            
            
            if event.type == pygame.KEYDOWN:
                if event.key == pygame.K_DOWN:
                    x_change = 0
                    y_change = 10
                elif event.key == pygame.K_UP:
                    x_change = 0
                    y_change = -10
                elif event.key == pygame.K_RIGHT:
                    x_change = 10
                    y_change = 0
                elif event.key == pygame.K_LEFT:
                    x_change = -10
                    y_change = 0
            




    dis.fill(black)
    wrap_position()
    pygame.draw.rect(dis,purple,(x,y,10,10))
    pygame.draw.rect(dis,pink,(foodx,foody, 10,10))
    pygame.display.update()
    clock.tick(30)


    pygame.quit()
    sys.exit()

game_loop()
