## 1. 使用git管理项目的基本操作(6个)
    1). 创建本地仓库
       a. 创建.gitignore文件, 指定需要忽略的文件/文件夹
       b. 创建工作区: git init
       c. 创建索引区: git add *
       d. 创建版本区: git commit -m "init"
    2). 创建远程仓库
       a. 登陆github
       b. New Repository
       c. 指定名称
       d. 确定创建
    3). 将本地仓库推送到远程
       a. 关联: git remote add origin https://github.com/zxfjd3g/180524_GitTest.git
       b. 推送: git push origin master
    4). 如果本地有修改, 推送到远程
      a. git add *
      b. git commit -m "update README.md"
      c. git push origin master
    5). 如果远程有修改, 拉取到本地
      a. git pull origin master
    6). 新来一个同事
      a. git clone url

## 2. git的3个分区
    1). 工作区: git init
    2). 暂存/索引区: git add *
    3). 版本区: git commit -m "xxx"
    
## 3. git的pull与fetch
    1). pull: 拉取远程的更新到本地仓库的当前分支, 并自动合并(可能会出冲突)
    2). fetch: 拉取远程的更新到本地仓库的新分支上, 需要手动合并到当前分支(可能会出冲突)

## 4. git的分支,合并与冲突
	1). 分支是在开发主线之外编写你的代码完成特定工作而不影响开发主线
	2). 分支的操作:
		查看分支: git branch
		创建分支: git branch dev
		切换分支: git checkout dev
		比较分支: git diff master dev
		合并分支: git merge dev
	3). 解决合并分支的冲突
		修正合并后产生冲突的代码
		git add *
		git commit -m "resolve conflict"   
    
## 5. 说说git公司多人协作与开源项目多人协作
    1). 公司多人协作: 先在github上创建组织(修改权限), 多个同事加入此组织, 在组织下创建项目, 成员都可以进行推送更新
    2). 开源多人协作: fork仓库到自己的账户下, 修改fork仓库的代码, 向原仓库发起一个pull request, 对方接收到请求后可以选择合并

## 6. github的2种请求方式
    1). https
        可以随意克隆github上的项目，而不管是谁的
        push的时候是需要验证用户名和密码的(麻烦)
    2). SSH
        克隆者必须是拥者或管理员，且需要先添加 SSH key ，否则无法克隆
        push的时候不再是验证用户名和密码，而是通过验证ssh的方式来验证用户
        	    