
1. Создайте учетную запись GitHub

https://github.com/join?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home

2. Установите CHOCOLATEY:
- запустите powershell от имени администратора
- выполните команду:
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```


3. Установите git на ваш ПК с помощью  Chocolatey:
```
choco install git -y
```
Вы можете использовать термінал git bash для работы с git, но я предпочитаю ConEmu. Эта программа поддерживает Ctrl+c и Ctrl+v и приятнее в использовании. Для того чтобы установить ConEmu необходимо выполнить команду:
```
choco install conemu
```

4. Настройте свой git:
```
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

5. Сгенерируйте новый SSH ключ:
```
ssh-keygen -t ed25519 -C "your_email@example.com"
```

6. Добавьте ключ в учетную запись Github:
- скопируйте /c/Users/you/.ssh/id_ed25519.pub 
- перейдите по ссылке https://github.com/settings/keys
- нажмите зеленую кнопку
![](https://github.com/maksym-peretiatko/labs-itm/blob/labs-en/lab1/Screenshot_2.png)

- установите скопированный ключ и нажмите зеленую кнопку
![](https://github.com/maksym-peretiatko/labs-itm/blob/labs-en/lab1/Screenshot_3.png)

Больше информации: https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

Теперь вы можете использовать GitHub

1. Создайте новый репозиторий

![](https://github.com/maksym-peretiatko/labs-itm/blob/labs-en/lab1/Screenshot_4.png)

Название репозитория должно быть таким же, как Ваш никнейм

![](https://github.com/maksym-peretiatko/labs-itm/blob/labs-en/lab1/Screenshot_5.png)

Убедитесь, что репозиторий публичный и проинициализирован с readme.md файлом

![](https://github.com/maksym-peretiatko/labs-itm/blob/labs-en/lab1/Screenshot_6.png)

2. Заберите копию репозитрия на локальный ПК:
- скопируйте ссылку
![](https://github.com/maksym-peretiatko/labs-itm/blob/labs-en/lab1/Screenshot_1.png)
- запустите команду для клонирования репозитрия:
```
git clone
```
В **моем** случае это:
```
git clone git@github.com:maksym-peretiatko/maksym-peretiatko.git
```

3. Откройте README.md вашим любимым текстовым редактором.

**maksym-peretiatko/maksym-peretiatko** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Here are some ideas to get you started:

- 🔭 I’m currently working on ...
- 🌱 I’m currently learning ...
- 👯 I’m looking to collaborate on ...
- 🤔 I’m looking for help with ...
- 💬 Ask me about ...
- 📫 How to reach me: ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

Вы можете использовать стандартный шаблон или создать свой собственный.

4. Напишите о себе
- С чем зотели бы поработать;
- Чем увлекаетесь;
- Добавьте ссылки на свои социальные сети и ресурсы, которые посчитаете нужными

5. Загрузите описание вашего профиля:
```
git add .
git commit -m "Add your comment"
git push

