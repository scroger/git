# GIT cheatsheet

# Config
```
git config --global user.name "[firstname lastname]"  
git config --global user.email "[email]"
```  
  
# Init or clone
```
git init  
git clone [url]
```  
  
# Work
```
git remote add origin [url]  
git pull  
git log  
git log --oneline  
git status  
git add [file]  
git rm [file]  
git commit -m "[commit message]"  
git push
```  
  
# Branch
```
git branch  
git branch [branch-name]  
git checkout -b [branch-name]
```  

# Хеш (идентификатор) коммита
> Информация о коммите — это набор данных: когда был сделан коммит, содержимое файлов в репозитории на момент коммита и ссылка на предыдущий, или родительский, коммит. Git хеширует эту информацию с помощью алгоритма SHA-1 и получает для каждого коммита свой уникальный хеш.

# Пример вывода команды ```git log```
```
commit e83c5163316f89bfbde7d9ab23ca2e25604af290
Author: Linus Torvalds <torvalds@linux-foundation.org>
Date:   Thu Apr 7 15:13:13 2005 -0700

Initial revision of "git", the information manager from hell
```

# HEAD
> Файл HEAD — один из служебных файлов папки .git. Он указывает на коммит, который сделан последним (то есть на самый новый).  
> Внутри HEAD — ссылка на служебный файл: refs/heads/master (или refs/heads/main в зависимости от названия ветки). Если заглянуть в этот файл, можно увидеть хеш последнего коммита.

# Статусы untracked/tracked, staged и modified
## untracked
> Новые файлы в Git-репозитории помечаются как untracked, то есть неотслеживаемые. Git «видит», что такой файл существует, но не следит за изменениями в нём. У untracked-файла нет предыдущих версий, зафиксированных в коммитах или через команду git add.

## staged
> После выполнения команды git add файл попадает в staging area (от англ. stage — «сцена», «этап [процесса]» и area — «область»), то есть в список файлов, которые войдут в коммит. В этот момент файл находится в состоянии staged.

## tracked
> Состояние tracked — это противоположность untracked. Оно довольно широкое по смыслу: в него попадают файлы, которые уже были зафиксированы с помощью git commit, а также файлы, которые были добавлены в staging area командой git add. То есть все файлы, в которых Git так или иначе отслеживает изменения.

## modified
> Состояние modified значит, что Git сравнил содержимое файла с последней сохранённой версией и нашёл отличия. Например, файл был закоммичен и после этого изменён.

# Пример вывода команды ```git status```
```
On branch master
Changes to be committed:
  (use "git restore --staged <file>..." to unstage)
          modified:   fileA.txt

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
          modified:   fileA.txt
```
