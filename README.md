##**Как создать SSH ключ**
#*Генерация SSH ключа*
1.Откройте Терминал. Вставьте в него следующий код, подставив в кавычки свой адрес электронной почты на GitHub.

```ssh-keygen -t ed25519 -C "your_email@example.com"```

2.Эта команда создает новый ключ SSH, используя введенный адрес электронной почты.

```Generating public/private ed25519 key pair.```

3.После вам будет предложено ввести название файла, в который сохранится ключ. Нажмите Enter, чтобы принять предложенное название и расположение файла по умолчанию.

```Enter a file in which to save the key (/Users/you/.ssh/id_ed25519):```[Press enter]

#*Добавление ключа в ssh-агент*
1.Запустите в терминале shh-agent.

```eval "$(ssh-agent -s)" > Agent pid 59566```

1.Добавьте свой приватный ключ SSH в ssh-agent. Если вы создали свой ключ под другим именем, замените id_ed25519 в команде именем вашего приватного ключа.

```$ ssh-add ~/.ssh/id_ed25519```

#*Как добавить ключ в аккаунт на GitHub*
1.Скопируйте содержание файла SSH ключа в буфер обмена

1.Откройте настройки пользователя (Settings) и выберите раздел SSH and GPG keys, или перейдите по ссылке https://github.com/settings /keys.

1.Кликните на New SSH key или Add SSH key.

1.В поле «Title» добавьте описание нового ключа. Например, если вы используете Малинку под номером 5, вы можете написать «RaspberryPi #5».

1.Вставьте ключ из буфера обмена в поле Key.

1.Нажмите "Add SSH key". Если будет предложено, введите пароль для подтверждения.

#*Как склонировать репозиторий*
1.Когда вы решите склонировать репозиторий, нужно нажать кнопку Clone, но вместо HTTPS выбрать SSH. Скопировать ссылку и выполнить команду git clone "скопированная ссылка.