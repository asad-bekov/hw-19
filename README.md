# Домашнее задание к занятию «Ветвления в Git»
*Асадбеков Асадбек*

### Выполненные этапы:

### 1. Инициализация репозитория и создание основных файлов
- Создан каталог `branching` в директории `hw-19`.
- Внутри `branching` созданы два скрипта:
  - `merge.sh`
  - `rebase.sh`

### 2. Создание основного коммита
- Выполнена команда:
  ```bash
  git add merge.sh rebase.sh
  git commit -m "prepare for merge and rebase"
  ```
- Коммит отправлен в ветку `main` в удалённые репозитории:
  ```bash
  git push origin main
  git push gitlab main
  git push bitbucket main
  ```

---

### 3. Работа с веткой `git-merge`
- Создана ветка `git-merge`:
  ```bash
  git checkout -b git-merge
  ```

#### Изменение 1:
- Внесены изменения в `merge.sh`:
  ```bash
  count=1
  for param in "$@"; do
      echo "\$@ Parameter #$count = $param"
      count=$(( $count + 1 ))
  done
  ```
- Коммит выполнен с сообщением:
  ```bash
  git commit -m "merge: @ instead *"
  ```

#### Изменение 2:
- Внесены изменения в `merge.sh` для использования `shift`:
  ```bash
  count=1
  while [[ -n "$1" ]]; do
      echo "Parameter #$count = $1"
      count=$(( $count + 1 ))
      shift
  done
  ```
- Коммит выполнен с сообщением:
  ```bash
  git commit -m "merge: use shift"
  ```
- Ветка `git-merge` отправлена в удалённые репозитории:
  ```bash
  git push -u origin git-merge
  git push -u gitlab git-merge
  git push -u bitbucket git-merge
  ```

---

### 4. Изменение `main` для `rebase.sh`
- Внесены изменения в `rebase.sh` в ветке `main`:
  ```bash
  count=1
  for param in "$@"; do
      echo "\$@ Parameter #$count = $param"
      count=$(( $count + 1 ))
  done

  echo "====="
  ```
- Изменения закоммичены и отправлены в `main`.

---

### 5. Работа с веткой `git-rebase`
- Создана ветка `git-rebase` от коммита `prepare for merge and rebase`:
  ```bash
  git checkout -b git-rebase <commit-hash>
  ```

#### Изменение 1:
- Внесены изменения в `rebase.sh`:
  ```bash
  for param in "$@"; do
      echo "Parameter: $param"
  done
  ```
- Коммит выполнен:
  ```bash
  git commit -m "git-rebase 1"
  ```

#### Изменение 2:
- Внесены изменения в `rebase.sh`:
  ```bash
  for param in "$@"; do
      echo "Next parameter: $param"
  done
  ```
- Коммит выполнен:
  ```bash
  git commit -m "git-rebase 2"
  ```
- Ветка `git-rebase` отправлена:
  ```bash
  git push -u origin git-rebase
  git push -u gitlab git-rebase
  git push -u bitbucket git-rebase
  ```

---

### 6. Слияние ветки `git-merge` в `main`
- Ветку `git-merge` слили в `main`:
  ```bash
  git checkout main
  git merge git-merge
  git push
  ```

---

### 7. Rebase ветки `git-rebase`
- Переключились в `git-rebase` и выполнили `rebase`:
  ```bash
  git checkout git-rebase
  git rebase main
  ```
- Возникли конфликты, которые были разрешены и подтверждены:
  ```bash
  git add rebase.sh
  git rebase --continue
  ```
- Изменения отправлены с `--force`:
  ```bash
  git push -f origin git-rebase
  git push -f gitlab git-rebase
  git push -f bitbucket git-rebase
  ```

---

### 8. Завершение работы
- Ветка `git-rebase` была успешно слита в `main`.
- Ветка `git-rebase` была удалена:
  ```bash
  git branch -d git-rebase
  git push origin --delete git-rebase
  git push gitlab --delete git-rebase
  git push bitbucket --delete git-rebase
  ```

Теперь граф имеет линейную структуру с `main` и `git-merge` как отдельной веткой.

### 4. Визуализация веток:

- Визуализация веток доступна на GitHub:  
  [Network Graph](https://github.com/asad-bekov/hw-19/network)
