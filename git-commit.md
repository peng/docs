提交与创建新代码到远程仓库

git init //初始化git  
git add [文件夹名或者文件名] //提交与新建都是这个命令  
git commit -m"提交的注释"  
git remote add origin "远程仓库的地址" // 第一次用以后就不用了 
git push -u origin master  //推送到远程主分支上

//=================

git 修改远程仓库地址

第一种方法
git remote set-url origin [url]

第二种方法
git remote rm origin
git remote add origin [url]


# Command line instructions

## Git global setup
```
git config --global user.name "myname"
git config --global user.email "myemailaddress"
```

## Create a new repository
```
git clone git/https-address-test
cd test
touch README.md
git add README.md
git commit -m "add README"
git push -u origin master
```

## Existing folder
```
cd existing_folder
git init
git remote add origin git/https-address-test
git add .
git commit -m "Initial commit"
git push -u origin master
```

## Existing Git repository
```
cd existing_repo
git remote rename origin old-origin
git remote add origin git/https-address-test
git push -u origin --all
git push -u origin --tags
```

## git提交信息规范  
feat|opti|fix|docs|style|refactor|perf|test|workflow|build|ci|chore|types|wip
* feat：新增功能  
* opti: 优化(样式/交互/逻辑)等  
* fix: 修复bug  
* docs: 修改文档  
* style：仅仅修改了空格、缩进等，不改变代码逻辑  
* refactor：代码重构，未新增任何功能和修复任何bug  
* perf：改善性能和体现的修改  
* test：测试用例的修改  
* workflow:  
* build: 改变构建流程，新增依赖库、工具等 （例如webpack修改)
* ci：自动化流程配置修改  
* chore：非src和test的修改  
* types:  
* wip: 移除文件或者代码 