# Шпаргалка по Git
## Термины
- Git - система контроля версий
- GitHub - удаленное хранилище репозиториев
## Команды
- git init - создание локального репозитория
- git add *название файла или --all* - добавление в репозиторий файлов
- git commit -m *сообщение* - создание коммита (сохранение изменений локального репозитория)
- git remote add origin *SSH-ссылка на удаленный репозиторий* - соединение локального и удаленного репозиториев
- git push - синхронизация локального и удаленного репозиториев
- хэш - уникальная последовательность символов, указывающая на тот или иной файл (меняется при изменении содержимого файла)
- Информация хэш -> информация о коммите содержится в папке .git/
- Лог - журнал записей о коммитах репозитория. Описание каждого коммита содержит хэш, имя автора, дату коммита, а также сообщение
- git log - получить лог
- git log --oneline - получить сокращенный лог (сокращенный хэш + сообщение)
- HEAD - служебный файл, указывает на сделанный последним коммит, может использоваться вместо хэша последнего коммита
## Статусы
- untracked - Git не следит за изменениями файла
- staged - файл попадет в коммит
- tracked - файл зафиксирован с помощью git commit, или же добавлен git add
- modified - Git нашел отличия между содержимым файлом и содержимым последней сохраненной версии файла

```mermaid
graph LR;
    untracked -- "git add" --> staged
    staged -- "git commit" --> tracked
    staged -- "изменения"  --> modified
    tracked -- "изменения" --> modified
    modified -- "git add"  --> staged
```

## Правила оформления комментариев к коммитам
- Комментарий должен быть содержательным
- Комментарий должен начинаться с глагола
- Стиль оформления комментария нередко бывает оговорен командой
