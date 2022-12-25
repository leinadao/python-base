# python-base
A base python setup

Set up in a repo:
```
  git remote add python-base git@github.com:leinadao/python-base.git
  git fetch python-base
  git rebase python-base/main # Resolve any conflicts.
  git push # possibly need --force
```
Update latest base changes in a repo:
```
  git fetch python-base
  git rebase python-base/main # Resolve any conflicts.
  git push # possibly need --force
```
