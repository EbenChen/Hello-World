# Hello-World
学习创建GitHub存储库，存储学习GitHub笔记
在Wiki里面有对初学的总结笔记

注意对branch的概念的理解：
master和feature都是branch
master是最终的主分支
feature是特征分支，是每一次做特征处理需要创建的，以mater为基础copy出来，修改完成后最终需要合并回master分支

pull request是针对已做了修改而言，修改了内容的feature branch即可以发起pull request
merge request是针对需要合进内容而言，这里指的master branch即可把发起合并的内容添加到master分支

学习Windows下的git bash，在官方https://git-for-windows.github.io/

windows下配置Github的SSH Key
先设置Github的user name 和 email
git config --global user.name "Git账号"
git config --global user.email "Git邮箱"

生成一个新的SSH密钥
打开Git Bash,输入如下命令，然后连续三个回车即可:
ssh-keygen -t rsa -C"your_email@example.com"
注:生成的SSH私钥路径后面会用到

将SSH私钥匙添加到ssh-agent
配置ssh-agent程序使用SSH key
1.在后台启动ssh-agent
eval $(ssh-agent -s)
2.将SSH私下钥添加到ssh-agent
ssh-add /c/User/chenjs/.ssh/iad-rsa
将SSH公钥添加到GitHub账户
配置GitHub账户使用SSH key
1.先复制SSH公钥的完整内容(/c/Users/chenjs/.ssh/id_rsa.pub)
2.进入GitHub的设置页面
测试连接
打开Git Bash输入:
ssh -T git@github.com
