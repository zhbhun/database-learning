## 教程

- [MongoDB 教程 - 菜鸟教程](https://blog.csdn.net/dongkeai/article/details/127330013)

### 安装

- [Mac OS](https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-os-x/)

### 管理服务

- Mac

  ```shell
  brew services start mongodb-community # 启动
  brew services stop mongodb-community # 关闭
  mongosh --eval "printjson(db.runCommand({whatsmyuri: 1}).you)" # 查看连接地址
  ```

FAQ

- [安装mongodb-community之后提示command not found: mongo找不到mongo指令](https://blog.csdn.net/dongkeai/article/details/127330013)

### 数据库

```shell
show dbs # 显示数据库
use DATABASE_NAME # 使用或创建数据库
db.dropDatabase() # 删除数据库
```

### 集合(表)

```shell
show collections # 查看当前数据库的所有集合
show tables # show collections 命令会更加准确点
db.createCollection("messages", { capped: true, autoIndexId: true, size: 1000, max: 1000 }) # 创建集合
db.messages.drop() # 删除数据库
```

### 文档(行)

```shell
db.messages.insert({title: 'MongoDB 教程', description: 'MongoDB 是一个 Nosql 数据库', by: '菜鸟教程', url: 'http://www.runoob.com', tags: ['mongodb', 'database', 'NoSQL'], likes: 100 }) # 插入行
db.messages.find().pretty() # 查询
```