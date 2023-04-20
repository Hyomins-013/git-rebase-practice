## Git Command

- `git rebase [-i]` : feature/브런치 에서 git rebase -i main 을 실행시키게 되면 feature/브런치 에서 적어놓았던 commit 메시지의 실행 시점을 main의 가장 최신화된 commit의 위치로 재배치된다.
rebase의 과정속에서 feature/브런치의 commit 들을 하나로 squash 를 하게 되는데 여러개의 커밋들 혹은 불필요한 커밋들을 하나로 압축 시킨뒤 원격저장소에 push 하게 된다.
- `git rebase --abort` : git rebase --abort는 rebase 하는 과정에서 너무나 많은 Conflict 가 발생하면 도중에 rebase를 실행했던 이전으로 되돌아 갈 수 있다.
- `git rebase --continue` : git rebase 과정속에서 Conflict 해결이 완료되면, rebase의 과정을 계속 이어 갈 수 있다. Conflict를 해결하고 난 뒤에는 git add . 를 통해 conflict 해결을 최신화 하되, 
**반드시 git commit 메시지를 남겨서는 안된다**
- `git reflog` : 내가 치명적인 실수를 저질렀거나, rebase의 과정속에서 혹은 merge, push 과정 속에서 과거로 되돌아 가고 싶을 때 사용한다. 커밋 내역들에 해쉬코드를 읽을 수 있는데, 이 해쉬코드를 사용해 돌아 갈 수 있다.
- `git reset` : git reflog 를 실행해서 찾아낸 해쉬코드를 git reset에 사용하여 과거의 코드로 되돌아 갈 수 있다.
