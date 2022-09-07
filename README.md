# Самоконтроль выполненения задания

1. Где расположен файл с `some_fact` из второго пункта задания?

По пути `group_vars/all/examp.yml`

2. Какая команда нужна для запуска вашего `playbook` на окружении `test.yml`?

Команда `ansible-playbook site.yml -i inventory/test.yml`

3. Какой командой можно зашифровать файл?

Командой `ansible-vault encrypt <путь к файлу>`, например `ansible-vault encrypt group_vars/el/examp.yml`

4. Какой командой можно расшифровать файл?

Командой `ansible-vault decrypt <путь к файлу>`, например `ansible-vault decrypt group_vars/el/examp.yml`

5. Можно ли посмотреть содержимое зашифрованного файла без команды расшифровки файла? Если можно, то как?

Командой `ansible-vault view <путь к файлу>`, `ansible-vault view group_vars/el/examp.yml`

6. Как выглядит команда запуска `playbook`, если переменные зашифрованы?

К ней добавляется параметр `--ask-vault-pass`, например:

`ansible-playbook site.yml -i inventory/prod.yml --ask-vault-pass`


7. Как называется модуль подключения к host на windows?

Модуль называется winrm.

8. Приведите полный текст команды для поиска информации в документации ansible для модуля подключений ssh

`ansible-doc -t connection ssh`


10. Какой параметр из модуля подключения `ssh` необходим для того, чтобы определить пользователя, под которым необходимо совершать подключение?

Параметр remote_user.