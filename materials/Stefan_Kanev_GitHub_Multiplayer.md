Това са събраните материали от нещата, които Стефан Кънев показа за Github Multiplayer.

_Добри практики_

__Commit Messages__

- 50/72 - 50 символа за първият ред от съобщението, 72 символа за по-описателната част
- http://stackoverflow.com/questions/2290016/git-commit-messages-50-72-formatting
- http://ablogaboutcode.com/2011/03/23/proper-git-commit-messages-and-an-elegant-git-history/
- https://wiki.openstack.org/wiki/GitCommitMessages
- http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html
- Спазването на консистентност е важно в случая.

__Rebase vs. Merge (Pull with Rebase)__

- Избягване на *Merge Bubbles* с цел по-чист `git log`
- http://stackoverflow.com/questions/804115/git-rebase-vs-git-merge
- `git pull` = `git fetch` + `git merge` по default
- `git pull --rebase` или http://blog.aplikacja.info/2010/11/git-pull-rebase-by-default/
- http://stackoverflow.com/questions/4684352/whats-a-fast-forward-in-git
- http://www.sbf5.com/~cduan/technical/git/git-5.shtml

_Модели за работа_

__Gitflow__

- https://github.com/nvie/gitflow
- Подходящ за приложения със строго определени версии
- Поддържа множество branch-ове : master, release, develop, feature-branches, hotfix
- Много "церемония"
- Изисква допълнителен Tool за работа

__Github Flow__

- http://scottchacon.com/2011/08/31/github-flow.html
- Подходящ за често deploy-ване (По няколко пъти на ден)

Поддържа 6 правила:

1. Anything in the master branch is deployable
2. To work on something new, create a descriptively named branch off of master (ie: new-oauth2-scopes)
3. Commit to that branch locally and regularly push your work to the same named branch on the server
4. When you need feedback or help, or you think the branch is ready for merging, open a pull request
5. After someone else has reviewed and signed off on the feature, you can merge it into master
6. Once it is merged and pushed to ‘master’, you can and should deploy immediately


__Skanev Flow__

- Смесица между горните два flow-a

1. Master is always deployable / stable
2. Production branch points to the current deployed version
3. Feature branches off master
4. Single commits to master are OK
5. Open pull request when ready with the feature
6. To close a pull request, *everyone in the team* should :shipit: