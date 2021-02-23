
1. Створіть обліковий запис GitHub

https://github.com/join?ref_cta=Sign+up&ref_loc=header+logged+out&ref_page=%2F&source=header-home

2. Встановіть CHOCOLATEY:
- запустіть powershell від імені адміністратора
- виконайте команду:
```
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://chocolatey.org/install.ps1'))
```


3. Встановіть git на ваш комп'ютер за допомогою Chocolatey:
```
choco install git -y
```
Ви можете використовувати термінал git bash для роботи з git Але я надаю перевагу ConEmu. Ця програма підтримує гарячі клавіші Ctrl+c і Ctrl+v та приємніша у користуванні. Для того щоб установити ConEmu необхідно виконати команду:
```
choco install conemu
```

4. Налаштуйте свій git:
```
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

5. Згенеруйте новий SSH ключ:
```
ssh-keygen -t ed25519 -C "your_email@example.com"
```

6. Додайте ключ до облікового запису Github:
- зкопіюйте /c/Users/you/.ssh/id_ed25519.pub 
- перейдіть за посиланням https://github.com/settings/keys
- натисніть зелену кнопку
![](Screenshot_2.png)

- Вставте зкопійований ключ та натисніть відповідну кнопку
![](.\Screenshot_3.png)

Більше інформації: https://docs.github.com/en/github/authenticating-to-github/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent

Тепер ви можете використовувати GitHub

1. Створіть новий репозиторій

![](Screenshot_4.png)

Назва репозиторію має бути такою як ваш нікнейм

![](Screenshot_5.png)

Переконайтеся, що репозиторій публічний та проініціалізований з readme.md файлом

![](Screenshot_6.png)

2. Заберіть копію репозиторію на локальний комп'ютер:
- зкопіюйте посилання
![](Screenshot_1.png)
- запустіть команду для клонування репозиторію:
```
git clone
```
У моєму випадку це:
```
git clone git@github.com:maksym-peretiatko/maksym-peretiatko.git
```

3. Відкрийте README.md вашим улюбленим текстовим редактором. 

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

Ви можете скористатися цим шаблоном або створити власний.

4. Напишіть про себе
- З чим хотіли б попрацювати;
- Чим захоплюєтесь;
- Додайте посилання на свої соціальні мережі та ресурси, які вважаєте необхідними або бажаними

5. Завантажте опис вашого профілю:
```
git add .
git commit -m "Add your comment"
git push

