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
    1. touch Makefile
    2. touch hello.py
    3. touch test_hello.py
    4. touch requirements.txt
    5. git remote -v
9. Enter these:
    1. python3 -m venv ~/.scaffold      -- where scaffold can be change
    2. source ~/.scaffold/bin/activate  -- where scaffold can be change
    3. which python                     -- to test
10. Enter codes into the 4 files
11. Enter into bash: make install
12. 
