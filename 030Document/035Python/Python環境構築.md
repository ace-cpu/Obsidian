---
created: 2025-11-03
tags:
  - Python
aliases:
related:
---

## Python 環境構築
　Pythonインストール　OriginalPython、anaconda
　Pip
　Git

### 実行環境
　ローカル、クラウド
　ファイル形式（.py）、ノートブック形式（.ipynb）


### 仮想環境　.venv（別の名前でも可）
　バージョン管理、パッケージ管理、ＯＳ依存
python -m venv .venv
.venv\Scripts\activate.bat
（pip でパッケージインストール）
deactivate

### anaconda
conda create --name myenv
conda activate myenv
conda deactivate

path
C:\Users\ace_a\anaconda3
C:\Users\ace_a\anaconda3\Library\mingw-w64\bin
C:\Users\ace_a\anaconda3\Library\usr\bin
C:\Users\ace_a\anaconda3\Library\bin
C:\Users\ace_a\anaconda3\Scripts

### pyenv-win
Invoke-WebRequest -UseBasicParsing -Uri "https://raw.githubusercontent.com/pyenv-win/pyenv-win/master/pyenv-win/install-pyenv-win.ps1" -OutFile "./install-pyenv-win.ps1"; &"./install-pyenv-win.ps1"
pyenv –version
pyenv install -l
pyenv install \<version\>
pyenv global \<version\>
pyenv versions

### Poetry
パス　C:\Users\ace_a\AppData\Roaming\Python\Scripts
poetry config virtualenvs.in-project true
poetry init
poetry install
poetry add numpy=1.24.0

## Pip
pip install パッケージ名\==1.1.1
pip list
pip list --outdated
pip install --upgrade パッケージ名

## Docker


## Pythonエディタ
Pycharm、VSCode
JupytorNote、Colaboratory


## Git & GitHub
### Git
git --version
git config --global user.email
git config --global user.name
git config --global user.name “ace-cpu”
git config --global user.email “55908070+ace-cpu@users.noreply.github.com”
git init　　－＞.git を作成
git status
git add .
git commit -m “Comment”　　コメント必ず必要

branch 名は main にする
git branch -m main
.gitignore ファイル　追跡ファイルに加える(git add)
　/.venv/


### GitHub
remote から GitHub へ
echo "# Imanyu50" >> README.md
git init
\## git config --global --add safe.directory "%(prefix)///$dir/Imanyu50"  (×’ 〇")
(git status)

\## git add README.md
git add .
git commit -m "first commit"
(git status)
git branch -M main
(git status)

git remote add origin https:\/\/\<USER\>:\<TOKEN\>@github.com/ace-cpu/\<PJT\>.git
git push -u origin main(:main)

GitHub から remote へ
git clone https\://\<USER\>:\<TOKEN\>@github.com/ace-cpu/\<PJT\>.git
git branch -a


## Jupyter notebook, Jupyter lab

### Jupyter  notebook
ルートディレクトリの変更
jupyter notebook --generate-config
$//jupyter_notebook_config.py
\## The directory to use for notebooks and kernels.
\#c.NotebookApp.notebook_dir = 'dir'

起動ディレクトリ指定
c.NotebookApp.notebook_dir = 'C:/Users/ace_a/Documents/MyPython'

### Jupyter lab
ルートディレクトリの変更
jupyter-lab --generate-config
$//jupyter_lab_config.py
\## DEPRECATED, use root_dir.
\#  Default: ''
\#c.ServerApp.notebook_dir = 'dir '

起動ディレクトリ指定
c.ServerApp.notebook_dir = 'C:/Users\ace_a/Documents/MyPython'
 
 
関連：
PowerShell　実行ポリシー
　現セッションのみ　Set-ExecutionPolicy RemoteSigned -Scope Process -Force
　現ユーザー　　　　Set-ExecutionPolicy RemoteSigned -Scope CurrentUser -Force
　Get-ExecutionPolicy
