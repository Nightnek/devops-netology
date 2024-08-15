# devops-netology

## Задание 1. Создать и настроить репозиторий для дальнейшей работы на курсе

В рамках курса вы будете писать скрипты и создавать конфигурации для различных систем, которые необходимо сохранять для будущего использования. Сначала надо создать и настроить локальный репозиторий, после чего добавить удалённый репозиторий на GitHub.

### Создание репозитория и первого коммита

1. Зарегистрируйте аккаунт на https://github.com/. Если предпочитаете другое хранилище для репозитория, можно использовать его.

![image](https://github.com/user-attachments/assets/fa3a11d2-1816-426c-a7c3-361985e5d98d)

2. Создайте публичный репозиторий, который будете использовать дальше на протяжении всего курса, желательное с названием devops-netology. Обязательно поставьте галочку Initialize this repository with a README.

https://github.com/Nightnek/devops-netology

3. Создайте авторизационный токен для клонирования репозитория.

![image](https://github.com/user-attachments/assets/8035944d-91d1-4133-807b-23340b7eb947)

4. Склонируйте репозиторий, используя протокол HTTPS (git clone ...).

![image](https://github.com/user-attachments/assets/6c8ac8b4-9914-44dd-8934-0963be68c1fa)

5. Перейдите в каталог с клоном репозитория (cd devops-netology).

![image](https://github.com/user-attachments/assets/fa82a9a6-40ca-46b9-af4c-a1c1c4f0e59e)

6. Произведите первоначальную настройку Git, указав своё настоящее имя, чтобы нам было проще общаться, и email (git config --global user.name и git config --global user.email johndoe@example.com).

![image](https://github.com/user-attachments/assets/ef09c8ea-ffc7-42c1-b84e-715784b0da87)

7. Выполните команду git status и запомните результат.

![image](https://github.com/user-attachments/assets/5cde14af-fffe-4902-8b83-f629c796cf6c)

8. Отредактируйте файл README.md любым удобным способом, тем самым переведя файл в состояние Modified.

9. Ещё раз выполните git status и продолжайте проверять вывод этой команды после каждого следующего шага.

![image](https://github.com/user-attachments/assets/3b227b3f-b04e-446b-a15d-3ca4c96c6b63)

10. Теперь посмотрите изменения в файле README.md, выполнив команды git diff и git diff --staged.

![image](https://github.com/user-attachments/assets/e02cb66f-119e-478c-9ced-5a67880aa9d0)
![image](https://github.com/user-attachments/assets/c2fb8642-a34f-4fbc-9d12-545d610eaaa4)

11. Переведите файл в состояние staged (или, как говорят, просто добавьте файл в коммит) командой git add README.md.

![image](https://github.com/user-attachments/assets/f35e71f6-d850-4b86-998b-d5959d41f049)

12. И ещё раз выполните команды git diff и git diff --staged. Поиграйте с изменениями и этими командами, чтобы чётко понять, что и когда они отображают.

![image](https://github.com/user-attachments/assets/b847dde5-8b2f-4917-9d5f-2c79710b762c)

13. Теперь можно сделать коммит git commit -m 'First commit'.

![image](https://github.com/user-attachments/assets/6e5ea3b2-29ed-4393-8133-8e4762607d0b)

14. И ещё раз посмотреть выводы команд git status, git diff и git diff --staged.

![image](https://github.com/user-attachments/assets/f060824f-5bd4-487b-8a11-59f465cf0cd6)

### Создание файлов .gitignore и второго коммита

1. Создайте файл .gitignore (обратите внимание на точку в начале файла), проверьте его статус сразу после создания.

   ![image](https://github.com/user-attachments/assets/35ea3ab2-33e6-4d6a-a31a-eb9b18ae9922)

3. Добавьте файл .gitignore в следующий коммит (git add...).
4. На одном из следующих блоков вы будете изучать Terraform, давайте сразу создадим соотвествующий каталог terraform и внутри этого каталога — файл .gitignore по примеру: https://github.com/github/gitignore/blob/master/Terraform.gitignore.

   ![image](https://github.com/user-attachments/assets/b41674cf-0842-480d-b35f-b0e162db3abb)

6. В файле README.md опишите своими словами, какие файлы будут проигнорированы в будущем благодаря добавленному .gitignore.

````
Будут проигнорированы файлы состояния Terraform, локальные папки, файлы с переменными(они могу содержать чувствительную информацию), файлы логов, Файлы конфигурации CLI Terraform, файлы отмен
````

5. Закоммитьте все новые и изменённые файлы. Комментарий к коммиту должен быть Added gitignore.

   ![image](https://github.com/user-attachments/assets/b4a7a65e-0b5f-435a-80bb-14f34c6f3ec1)


### Эксперимент с удалением и перемещением файлов (третий и четвёртый коммит)

1. Создайте файлы will_be_deleted.txt (с текстом will_be_deleted) и will_be_moved.txt (с текстом will_be_moved) и закоммите их с комментарием Prepare to delete and move.

   ![image](https://github.com/user-attachments/assets/258f5ebc-8060-4c22-8869-388a4ca769d4)

3. В случае необходимости обратитесь к официальной документации — здесь подробно описано, как выполнить следующие шаги.
4. Удалите файл will_be_deleted.txt с диска и из репозитория.

   ![image](https://github.com/user-attachments/assets/7a5e31ba-cfd9-4105-8338-9f17d857b37a)

6. Переименуйте (переместите) файл will_be_moved.txt на диске и в репозитории, чтобы он стал называться has_been_moved.txt.

   ![image](https://github.com/user-attachments/assets/aa58122b-bd67-4a17-bd76-bc7f13c1fce0)

8. Закоммитьте результат работы с комментарием Moved and deleted.

   ![image](https://github.com/user-attachments/assets/9922e31e-64bb-4c23-9d69-3df24899dca9)


### Проверка изменения

1. В результате предыдущих шагов в репозитории должно быть как минимум пять коммитов (если вы сделали ещё промежуточные — нет проблем):
    * `Initial Commit` — созданный GitHub при инициализации репозитория. 
    * `First commit` — созданный после изменения файла `README.md`.
    * `Added gitignore` — после добавления `.gitignore`.
    * `Prepare to delete and move` — после добавления двух временных файлов.
    * `Moved and deleted` — после удаления и перемещения временных файлов. 
2. Проверьте это, используя комманду `git log`. Подробно о формате вывода этой команды мы поговорим на следующем занятии, но посмотреть, что она отображает, можно уже сейчас.

   ![image](https://github.com/user-attachments/assets/c1833b32-897b-43b5-a8a3-0e01f7b33adb)
