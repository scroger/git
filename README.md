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
