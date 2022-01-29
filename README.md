### Hi there 👋

<!--
**botsol/botsol** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...
-->
# Тут нарисуем наш шарик, называем этот объект точно также как и класс в коде

<PongBall>:

size: 50, 50

canvas:

Ellipse:

pos: self.pos

size: self.size

# Тут нарисуем панельку игрока, называем этот объект точно также как и класс в коде

<PongPaddle>:

size: 25, 200

canvas:

Rectangle:

pos: self.pos

size: self.size

# А это игровое поле =)

<PongGame>:

## тут привязываем шарик к свойству ball

ball: pong_ball

player1: player_left

player2: player_right

canvas:

Rectangle:

## Бордюр посередине

pos: self.center_x - 5, 0

size: 10, self.height

Label:

## Очки игрока слева

font_size: 70

center_x: root.width / 4

top: root.top - 50

text: str(root.player1.score)

Label:

## Очки игрока справа

font_size: 70

center_x: root.width * 3 / 4

top: root.top - 50

text: str(root.player2.score)

## а тут создаем экземпляр нашего шарика в игровом поле

PongBall:

id: pong_ball

center: self.parent.center

## создаем игрока 1

PongPaddle:

id: player_left

x: root.x

center_y: root.center_y

## создаем игрока 2

PongPaddle:

id: player_right

x: root.width - self.width

center_y: root.center_y
