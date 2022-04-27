## 開発手順
* [要件定義](https://qiita.com/Saku731/items/741fcf0f40dd989ee4f8) を参照

<img width="678" alt="image" src="https://user-images.githubusercontent.com/39234092/165414807-6d91d2a0-fca1-47a7-9c48-c7e3e7700ee5.png">

### task管理
* githubのProjectsで行う

<img width="977" alt="image" src="https://user-images.githubusercontent.com/39234092/165415049-ade0491f-fd13-4e88-b4e6-5e93ba808d6b.png">

### スクラム 
* 以下の用語を押さえる
    * スプリント
    * レトロ
    * To do(issue)
    * epics
    * フィボナッチ係数
    * icebox
    * in Progress
    * done
    * closed
    * velocity

<img width="1205" alt="image" src="https://user-images.githubusercontent.com/39234092/165415353-68731b71-fe5e-42c1-ac8c-b67f3e0c4cdc.png">

### push
* 1日1push
* push前に
    * 差分(`$ git diff`)を確認しておく
    * linterを掛けておく(rubocopなど)
    * testをpassさせる

### pull request
* pushしたらpull requestする(main branchへのmerge依頼)

<img width="840" alt="image" src="https://user-images.githubusercontent.com/39234092/165416551-b14c7455-2718-41ae-ac08-55359adc5906.png">

* pull requestしたら、File changedでも変更点を確認

<img width="788" alt="image" src="https://user-images.githubusercontent.com/39234092/165416638-d6d8f639-7fcd-48e9-9278-4be77532495d.png">


### 開発での心がけ
* branchは切る
* 不要な変更はしない(改行入れるだけなど)
    * 必要な変更だけをする、確認者がレビューし易くする為です


### test
* testはrspecを使用
* `$ rspec spec/system`

### circleCI
* pushすると、自動でcircleCIという自動testが動く
    * localでpassしていたら問題ないが、localでtestせずにpushしてしまう事もある為
    * pushしてからfail(testに落ちる)してしまうと、修正して再度pushする手間が発生する為、最初にlocalでtestしておく
    * testにpassするとcheckが、落ちるとxが付く

<img width="797" alt="image" src="https://user-images.githubusercontent.com/39234092/165416996-e775563b-fd2c-46f0-8a58-05e9d6c9d5d5.png">
