## 教程

- [MongoDB 教程 - 菜鸟教程](https://blog.csdn.net/dongkeai/article/details/127330013)

### 管理服务

- Mac

  ```shell
  brew services start mongodb-community # 启动
  brew services stop mongodb-community # 关闭
  mongosh --eval "printjson(db.runCommand({whatsmyuri: 1}).you)" # 查看连接地址
  ```

FAQ

- [安装mongodb-community之后提示command not found: mongo找不到mongo指令](https://blog.csdn.net/dongkeai/article/details/127330013)