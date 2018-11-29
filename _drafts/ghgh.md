---
title: ghgh
layout: post
date: 2018-11-29 13:05:26 +0000

---
\# Совместное использование android-устройств с помощью openstf

\---------------------------------------------------------------

!\[\](![](https://raw.githubusercontent.com/openstf/stf/master/res/common/logo/exports/STF-128.png))

\* Устанавливаем docker-compose - [https://docs.docker.com/compose/install/#prerequisites](https://docs.docker.com/compose/install/#prerequisites "https://docs.docker.com/compose/install/#prerequisites")

\* Берем Dockerfile - [https://github.com/openstf/stf/blob/master/Dockerfile](https://docs.docker.com/compose/install/#prerequisites "https://docs.docker.com/compose/install/#prerequisites")

\* переходим в папку в которой лежит Dockerfile и выполняем - *docker-compose up*, 

\* а т.к нам нужно будет найти публичный ip в логах, стоит выполнить:

 \`\`\`bash

  docker-compose up | grep --color -E 'app-url|$' 

\`\`\`

\* В выводе публичный ip будет напротив выделенного цветом(красным) *app-url*, что-то вроде:

!\[\](![](https://i.snag.gy/75x0tR.jpg))

\* Как только мы подняли openstf, он уже следит за подключенными usb-девайсами, 

 если желаемое устройство уже подключено, то в логах можно увидеть следующее:

!\[\](![](https://i.snag.gy/LIed6G.jpg))

\* Если же мы подключаем девайс после выполнение команды, то в логах будет:

!\[\](![](https://i.snag.gy/IwDvOp.jpg))

\* Открываем страницу по найденному адресу и заполняем поля любыми, удовлетворяющими валидации, значениями

!\[\](![](http://4009.jp/post_assets/376/160229/stf_og.jpg))

\* После мы будем перекинуты сразу на страницу с подключенными девайсами

!\[\](![](https://i.snag.gy/LwPVtY.jpg))