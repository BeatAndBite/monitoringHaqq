# monitoringHaqq
Это гайд к системе мониторинга в телеграмме с помощью бота @BotFather которая будет оповещать о состоянии вашего узла, пропущенных блоках в неактивном статусе.Также она каждый час отправляет вам краткую информацию о статусе вашего узла.

  Инструкция:
    1. Создаем телеграмм-бота через @BotFather, настройте его и get bot API token (инструкция <a href="https://www.siteguarding.com/en/how-to-get-telegram-bot-api-token">здесь</a>).
    2. Создаем 2-е группы: alarm и log. Настраиваем их, добавьте своего бота в свои чаты и get chats IDs (инструкция <a href="https://stackoverflow.com/questions/32423837/telegram-bot-how-to-get-a-group-chat-id" rel="nofollow">здесь</a>).
    3. Подключитесь к вашему серверу и создайте status папку в $HOME directory файле <code>mkdir $HOME/status/</code>.
    4. В этой папке $HOME/status/ вы должны создать cosmos.sh файл с расширением nano $HOME/status/cosmos.sh. Копируем всё содержимое из cosmos.sh в этом репозитории и вставляем в свой файл cosmos.sh .
    5. В этой папке $HOME/status/ вы должны создать haqq.conf файл с расширением nano $HOME/status/haqq.conf. В него внесите свои значения.Файл haqq.conf находится в этом репозитории.
    6. Установите несколько пакетов с расширением sudo apt-get install jq sysstat bc smartmontools fdisk -y.
    7. Установите пакеты с помощью <code>sudo apt-get install jq sysstat bc smartmontools fdisk -y</code>.

