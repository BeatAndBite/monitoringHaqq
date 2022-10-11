# monitoringHaqq
Это гайд к системе мониторинга в телеграмме с помощью бота @BotFather которая будет оповещать о состоянии вашего узла, пропущенных блоках в неактивном статусе.Также она каждый час отправляет вам краткую информацию о статусе вашего узла.

  <p>Инструкция:</p>
    <ol>
    <li> Создаем телеграмм-бота через @BotFather, настройте его и get bot API token (инструкция <a href="https://www.siteguarding.com/en/how-to-get-telegram-bot-api-token">здесь</a>).</li>
    <li> Создаем 2-е группы: alarm и log. Настраиваем их, добавьте своего бота в свои чаты и get chats IDs (инструкция <a href="https://stackoverflow.com/questions/32423837/telegram-bot-how-to-get-a-group-chat-id" rel="nofollow">здесь</a>).</li>
    <li> Подключитесь к вашему серверу и создайте status папку в $HOME directory файле <code>mkdir $HOME/status/</code>.</li>
    <li> В этой папке $HOME/status/ вы должны создать cosmos.sh файл с расширением nano $HOME/status/cosmos.sh. Копируем всё содержимое из cosmos.sh в этом репозитории и вставляем в свой файл cosmos.sh .</li>
    <li> В этой папке $HOME/status/ вы должны создать haqq.conf файл с расширением nano $HOME/status/haqq.conf. В него внесите свои значения.Файл haqq.conf находится в этом репозитории.</li>
    <li> Установите несколько пакетов с расширением sudo apt-get install jq sysstat bc smartmontools fdisk -y.</li>
    <li> Установите пакеты с помощью <code>sudo apt-get install jq sysstat bc smartmontools fdisk -y</code>.</li>
    <li> Запустите bash cosmos.sh, чтобы проверить настройки. Если так то все Вы настроили верно - Нормальный вывод:
<code> root@duckduckduck:~/status# bash cosmos.sh

exp/me >>>>>> 247490/247490.

gap >>>>>>>>> 0 blocks.

chain >>>>>>> alive.

consensus >>> 0.00.

block_time >> 6.33 sec.

priv_key >>>> right.

_active >>>>> false.

gov >>>>>>>>> no unvoted proposals.

_upgrade >>>> v1.1.0.

_time_left >> 11h 28m.

_appr_time >> Oct 9, 16:36.

root@duckduckduck:~/status# </code>
  <li>Добавьте несколько правил с помощью <code>chmod u+x $HOME/status/cosmos.sh</code>.</li>
  <li>Отредактируйте crontab с помощью <code>crontab -e</code>.
    <p><code>1,11,21,31,41,51 * * * * bash $HOME/status/cosmos.sh >> $HOME/status/cosmos.log 2>&1</p></code>
  <li>Проверьте свои журналы с помощью <code>cat $HOME/status/cosmos.logили tail $HOME/status/cosmos.log -f</code></li>.
  </ol>

