- 👋 Hi, I’m @qqpp2
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
qqpp2/qqpp2 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->



import pygame

# 游戏地图大小
MAP_SIZE = 10

# 窗口大小
WINDOW_WIDTH = 800
WINDOW_HEIGHT = 600

# 方块大小
BLOCK_SIZE = WINDOW_WIDTH // MAP_SIZE

# 初始化Pygame
pygame.init()

# 创建窗口
window = pygame.display.set_mode((WINDOW_WIDTH, WINDOW_HEIGHT))
pygame.display.set_caption("3D Colorful Game")

# 游戏循环
running = True
while running:
    # 处理事件
    for event in pygame.event.get():
        if event.type == pygame.QUIT:
            running = False
    
    # 绘制地图
    for i in range(MAP_SIZE):
        for j in range(MAP_SIZE):
            if i == player_y and j == player_x:
                color = (255, 0, 0)  # 玩家位置红色
            else:
                color = (0, 255, 0)  # 空地绿色
            pygame.draw.rect(window, color, (j*BLOCK_SIZE, i*BLOCK_SIZE, BLOCK_SIZE, BLOCK_SIZE))
    
    # 更新窗口
    pygame.display.flip()

# 退出游戏
pygame.quit()
