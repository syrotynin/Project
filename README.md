Project
=======
Разработка продолжается.
<a href="https://github.com/syrotynin/Project/issues/1">Комментарии</a>
Идея:
Игроку на выбор предоставляется сыграть одну из песен в стиле рок. 5 клавиш клавиатуры играют роль “струн”. По экрану сверху вниз падают шары 5 цветов - “ноты”. Внизу находятся “струны” в виде кругов. При пересечении “ноты” и “струны” игроку необходимо нажать соответствующую клавишу на клавиатуре. В случае своевременного нажатия клавиши игрок зарабатывает очки. 
Основные возможности:

1.	Игра хранит имя(ник) пользователя.
2.	“Ноты” появляются сверху, исчезают – снизу.
3.	Ведется подсчет очков за удачно сыгранные ноты.
4.	“Струны” подсвечиваются при нажатии. 
5.	При нажатии неправильной “струны” или пропуска ноты громкость песни снижается и проигрывается звук “ошибки”.
6.	Игра хранит состояния песен(количество набранных очков и сыгранных песен)
7.	Имя и резульат игрока, набравшего наибольшее количество очков за песню, отображается в стадии игры соответственно выбраной песни.
Подробное описание возможностей:
1.	Размер окна 800x600.
2.	На фоне стадии игры изображен гриф гитары в увеличенном виде.
3.	Порядок генерации нот задается в коде, т.к. он специфичен для конкретной песни.
4.	Скорость падения нот зависит от сложности песни.
5.	Скорость падения нот не меняется на протяжении одной песни.
6.	При пересечении ноты и струны игрок получает константное количество очков за ноту соответствующей песни.
7.	В момент времени удачного пересечения ноты и струны нота исчезает с экрана, а громкость песни остается высоким.
8.	При неудачном нажатии кнопки(струны) срабатывает звук ошибки и громкость песни снижается в 2 раза.
9.	В случае если нота не была “сыграна” громкость песни снижается в 2 раза.
10.	При достижении определенного количества ошибок игрок проигрывает. Количество допустимых ошибок зависит от сложности песни.
11.	Размер ноты константен и меньше или равен размеру струны.
12.	В случае достижения пользователем рейтинга большего, чем у топового игрока, пользователь становится лидером (имя и количество очков сохраняются)

14.	Главное меню состоит из пунктов:
•	New game
•	Help
•	Quit

15.	Игроку предлагается ввести имя пользователя для подсчета статистики.
16.	В нижнем правом углу ведется подсчет очков игрока в тот момент, когда он непосредственно находится в стадии игры.
17.	В верхнем правом углу пишется текущий лучший резуьтат и имя игрока.
Доп. Информация:
Игра находится в стадии разработки. Планируется сделать редактор песен для создания наборов “нот”.

Полиморфизм: базовый абстрактный класс GameState-> от него наследуются состояния игры. В main'е состояния путем приведения к указателю базового класса переключаются между собой.
