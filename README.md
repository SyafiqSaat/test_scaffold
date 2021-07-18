[![Python application test with Github Actions](https://github.com/SyafiqSaat/test_scaffold/actions/workflows/main.yml/badge.svg)](https://github.com/SyafiqSaat/test_scaffold/actions/workflows/main.yml)

# test_scaffold - review
This is a Cloud Computing Foundation Week 3 **"Review GitHub Actions GitHub Project"**.


## How to create workflow from scratch
1. Generate SSH from code (add image)
2. Enter into bash: ssh-keygen -t rsa
3. Enter into bash: cat (/home/ec2-user//.ssh/id_rsa.pub) --in brackets should be copied from part 2
4. Copy key into SSH in GitHub settings
5. Enter into bash: git clone
6. Follow by Copy link into bash from git SSH 
7. Change file directory to write: $ cd scaffold/ -- where scaffold can be change
8. Enter the following to make file: 
    1. touch Makefile         --file #1
    2. touch hello.py         --file #2
    3. touch test_hello.py    --file #3
    5. touch requirements.txt --file #4
    6. git remote -v
9. Enter these:
    1. python3 -m venv ~/.scaffold      -- where scaffold can be change
    2. source ~/.scaffold/bin/activate  -- where scaffold can be change
    3. which python                     -- to test
10. Enter codes into the 4 files
11. Enter into bash:
    1. git status
    2. git add *
    3. git commit -m "adding initial structure"
    4. git config --global user.name "Syafiq Sa'at"
    5. git config --global user.email syafiqsaat2711@gmail.com
    6. git commit --amend --reset-author
    7. git push
12. Enter yaml language in actions:
```yaml
name: Python application test with Github Actions
on: [push]

jobs:
  build:

    runs-on: ubuntu-latest

    steps:
    - uses: actions/checkout@v2
    - name: Set up Python 3.8
      uses: actions/setup-python@v1
      with:
        python-version: 3.8
    - name: Install dependencies
      run: |
        make install
    - name: Lint with pylint
      run: |
        make lint
    - name: Test with pytest
      run: |
        make test
    - name: Format code
      run: |
        make format
```
    
