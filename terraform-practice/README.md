# 実践Terraform　AWSにおけるシステム設計とベストプラクティス 

https://amzn.asia/d/cqroK09

# 環境準備
- AWS
  - アカウント
  - IAM(AdministratorAccess)
- AWS CLI
  - ```pip install awscli --upgrade```
  - ```aws --version```
- AWSアクセスキーID、シークレットアクセスキーを環境変数に追加
- Terraformのインストール(https://developer.hashicorp.com/terraform/tutorials/aws-get-started/install-cli)
  - mac:
    - Homebrew( +tfenv, Dockernized Terraform)が紹介されていた
  - windows:
    - 方法1:公式サイトからzipダウンロード＆解凍
    - 方法2:Chocolateyでインストール ←こっちを採用する
    - 参考：https://c.itdo.jp/technical-information/system-manage/chocolatey/
  - Chocolateyを使用する方法(https://chocolatey.org/install)
    - Chocolateyをインストールする
      - PowerShell(管理者)を開く
      - コマンドを実行  
        ```Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))```
      - ```choco```コマンドが使えるようになればOK
    - Chocolateyでterraform をインストールする
      - ```choco install terraform```
      - ```terraform -help```でサブコマンドが表示できればインストール成功

Chocolatey

複数のソフトを一気にインストールできて便利
```例:cinst googlechrome git notepadplusplus firefox 7zip visualstudiocode vlc putty libreoffice winscp sourcetree slack -y```
