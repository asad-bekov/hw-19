# Домашнее задание к занятию «Системы контроля версий»

*Асадбеков Асадбек* 

# Это мой репозиторий для курса DevOps Netology

### Инициализация и первый коммит

1. Репозиторий создан на GitHub и инициализирован с `README.md`.
2. Клонирован с помощью HTTPS.
3. Выполнена базовая настройка Git (`user.name`, `user.email`).
4. Файл `README.md` отредактирован — добавлен заголовок.
5. Выполнены команды `git status`, `git diff`, `git diff --staged` для понимания текущего состояния.
6. Изменения были добавлены в staged и закоммичены с сообщением `First commit`.

---

### Добавление `.gitignore` и второй коммит

<<<<<<< HEAD
1. Создан файл `.gitignore`.
2. Создан каталог `terraform/` и файл `terraform/.gitignore` со следующим содержимым:
=======
### 1. Работа с GitLab:

- В `GitLab` был добавлен удалённый репозиторий:
  ```bash
  git remote add gitlab git@gitlab.com:asad-bekov/devops-netology.git
  ```

- Ветка `main` была отправлена в `GitLab`:
  ```bash
  git push -u gitlab main
  ```

- Ветка `fix` была также отправлена в `GitLab`:
  ```bash
  git push -u gitlab fix
  ```

- Теги `v0.0` и `v0.1` были отправлены в `GitLab`:
  ```bash
  git push gitlab v0.0
  git push gitlab v0.1
  ```
---

### 2. Работа с Bitbucket:

- В `Bitbucket` был создан проект `devop-net` и добавлен репозиторий `devops-netology`.
- В `Bitbucket` подключён SSH и настроен `remote`:
  ```bash
  git remote add bitbucket git@bitbucket.org:devop-net/devops-netology.git
  ```

- Ветка `main` была отправлена в `Bitbucket`:
  ```bash
  git push -u bitbucket main
  ```

- Ветка `fix` была также отправлена в `Bitbucket`:
  ```bash
  git push -u bitbucket fix
  ```

- Теги `v0.0` и `v0.1` были отправлены в `Bitbucket`:
  ```bash
  git push bitbucket v0.0
  git push bitbucket v0.1
  ```

---

### 3. Создание тегов:
>>>>>>> c8f83b1 (newest README.md)

*/.terraform/
*.tfstate
.tfstate.
crash.log
*.tfvars
override.tf
override.tf.json
*_override.tf
*_override.tf.json
.terraformrc
terraform.rc


3. В файл `README.md` добавлено пояснение о файлах, исключаемых из репозитория.

> **Какие файлы будут проигнорированы:**
> - `.terraform/` каталоги
> - файлы состояния `*.tfstate`
> - файлы переменных `*.tfvars`
> - override-конфигурации и логи
> - локальные настройки CLI

4. Все изменения закоммичены с сообщением `Added gitignore`.

---

<<<<<<< HEAD
### Удаление и перемещение файлов (эксперимент)
=======
### 4. Создание новой ветки `fix`:
>>>>>>> c8f83b1 (newest README.md)

1. Созданы два файла:
   - `will_be_deleted.txt` с содержимым `will_be_deleted`
   - `will_be_moved.txt` с содержимым `will_be_moved`
2. Оба файла добавлены в репозиторий и закоммичены с сообщением `Prepare to delete and move`.
3. Выполнено:
   - Удаление файла `will_be_deleted.txt` через `git rm`
   - Переименование `will_be_moved.txt` в `has_been_moved.txt` через `git mv`
4. Изменения закоммичены с сообщением `Moved and deleted`.

---

<<<<<<< HEAD
### Проверка истории
=======
### 5. Ссылки на репозитории:
>>>>>>> c8f83b1 (newest README.md)

В результате работы в истории коммитов (`git log --oneline`) отображаются следующие ключевые изменения:

- Initial commit (при инициализации репозитория)
- First commit (редактирование README)
- Added gitignore (добавление .gitignore файлов)
- Prepare to delete and move (создание временных файлов)
- Moved and deleted (удаление и переименование файлов)

---

<<<<<<< HEAD
### Отправка изменений
=======
### 6. Визуализация веток и тегов:
>>>>>>> c8f83b1 (newest README.md)

Все коммиты успешно отправлены на удалённые репозитории (`GitHub`, `GitLab`, `Bitbucket`) с помощью:

<<<<<<< HEAD
```bash
git push origin main
git push gitlab main
git push bitbucket main

- Теги `v0.0` и `v0.1` доступны на всех платформах. В GitHub они видны на странице [Tags](https://github.com/asad-bekov/devops-netology/tags).

---

### Итог:
Теперь репозиторий содержит ветку `fix` с изменениями в `README.md`, которая была создана на основе коммита `Prepare to delete and move`. Ветки синхронизированы между GitHub, GitLab и Bitbucket, а также созданы и запушены теги `v0.0` и `v0.1`.
