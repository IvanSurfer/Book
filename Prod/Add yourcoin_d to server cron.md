
Добавляем демона <yourocoin>d в cron сервера
--------------------------------------------

Процесс добавления демона монеты в `cron` необходим для того чтобы при перезапуске сервера демон поднимался автоматически


### Подключаемся к нашей мастер ноде с помощью SSH как User

[См. Подключение к серверу через SSH-клиент Bitvise](Addiction_masternode.md#Подключение-к-серверу-через-ssh-клиент-bitvise)

### Добавляем задание в Crontab

Чтобы отредактировать файл crontab, введите следующую команду в командной строке

	crontab -e

Переходим в самый конец файла и добавляем следующую строку:

	@reboot <полный/путь/до/демона/вашей/монеты>
*Например `/home/<имя_пользователя>/демон_монеты`*

После этого сохранем изменения.

Для просмотра `crontab` можно выполнить команду

	crontab -l

### Тестируем

- Перезапускаем сервер
- Открываем htop
- Ищем процесс с именем нашего демона например `testcoind`

The End