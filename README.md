# Git
## Git Pull and Git Fetch
### Git Pull:
The **"git pull"** command is a combination of two other Git commands: *"git fetch"* and *"git merge"*. It fetches changes from the remote repository and automatically merges them into the current branch.
### Git Fetch:
The **"git fetch"** command only retrieves changes from the remote repository but does not automatically merge them into the current branch. Instead, it updates the remote-tracking branches.

The most significant difference between **"git pull"** and **"git fetch"** is that **"git pull"** automatically merges the fetched changes into the current branch, while **"git fetch"** does not. This makes **"git pull"** a more convenient command if you want to quickly update your local branch with changes from the remote repository.  
When using **"git pull"**, the changes are merged directly into the local branch. On the other hand, **"git fetch"** updates the remote-tracking branches, which are references to the state of the remote branches in the remote repository.

Using **"git fetch"** can be considered safer than **"git pull"** since it does not modify your working directory or current branch until you explicitly merge the changes. This gives you more control over when and how you want to integrate the fetched changes into your code.
## Изменение последнего коммита: 
git commit --amend

Команда **git commit --amend** — это удобный способ изменить последний коммит. Она позволяет объединить проиндексированные изменения с предыдущим коммитом без создания нового коммита. Ее можно использовать для редактирования комментария к предыдущему коммиту без изменения состояния кода в нем. Но такое изменение не только редактирует последний коммит, но и полностью его заменяет. То есть измененный коммит станет новой сущностью с отдельной ссылкой. Для Git он будет выглядеть как новый коммит, который отмечен звездочкой (*) на схеме внизу. Существует несколько распространенных сценариев использования команды **git commit --amend**:
1. Изменение комментария к последнему коммиту Git
```
git commit --amend -m "an updated commit message"
```
3. Изменение файлов после коммита
```
# Edit hello.py and main.py
git add hello.py
git commit 
# Realize you forgot to add the changes from main.py 
git add main.py 
git commit --amend --no-edit
```
![Git amend](https://wac-cdn.atlassian.com/dam/jcr:34fd0826-9e89-4ef1-bce8-b1325cf48306/01-02%20Changing%20the%20Last%20Commit.svg?cdnVersion=2123)
