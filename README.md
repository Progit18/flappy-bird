
def flappygame():
    your_score = 0
    horizontal = int(window_width/5)
    vertical = int(window_width/2)
    ground = 0
    mytempheight = 100
 
def isGameOver(horizontal, vertical, up_pipes, down_pipes):
    if vertical > elevation - 25 or vertical < 0:
        return True
    for pipe in up_pipes:
        pipeHeight = game_images['pipeimage'][0].get_height()
        if(vertical < pipeHeight + pipe['y'] and
        abs(horizontal - pipe['x']) < game_images['pipeimage'][0].get_width()):
            return True

def createPipe():
    offset = window_height / 3
    pipeHeight = game_images['pipeimage'][0].get_height()

if __name__ == "__main__":
    pygame.init()
    framepersecond_clock = pygame.time.Clock()
    pygame.display.set_caption('FLAPPY BIRD')
    game_images['scoreimages'] = (
        pygame.image.load('image/0.png').convert_alpha(),
        pygame.image.load('image/1.png').convert_alpha(),
        pygame.image.load('image/2.png').convert_alpha(),
        pygame.image.load('image/3.png').convert_alpha(),
        pygame.image.load('image/4.png').convert_alpha(),
        pygame.image.load('image/5.png').convert_alpha(),
        pygame.image.load('image/6.png').convert_alpha(),
        pygame.image.load('image/7.png').convert_alpha(),
        pygame.image.load('image/8.png').convert_alpha(),
        pygame.image.load('image/9.png').convert_alpha(),
    )
    game_images['flappybird'] = pygame.image.load('image/bird.png').convert_alpha()
    game_images['sea_level'] = pygame.image.load('image/base.jfif').convert_alpha()
    game_images['background'] = pygame.image.load('image/background.jpg').convert_alpha()
    game_images['pipeimage'] = (pygame.transform.rotate(pygame.image.load('image/pipe.png').convert_alpha(),180),pygame.image.load('image/pipe.png').convert_alpha())

   
