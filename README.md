

# 克隆远程仓库

如果本地主机尚未与github账户关联，可以参考👇链接。

https://docs.github.com/cn/github/authenticating-to-github/adding-a-new-ssh-key-to-your-github-account

克隆仓库到本地

```shell
git clone git@github.com:riverhood/capa-rules.git
```

# 工作流

## 新增规则

如果新增的规则不在[【腾讯文档】八类行为规则筛选](https://docs.qq.com/sheet/DZGFxZHphQ0hXd01U)中，请在腾讯文档中添加新的筛选条件，并设置字体颜色为红色.

- 新增未验证的规则：

  在规则目录的to-verify文件夹新建规则，规则的`name`与`namescope`按需要编写，`author`为<u>to-verify-自己的名字</u>，以便以后验证。然后运行以下命令更新到github远程仓库。

  ```shell
  git add 所有新建规则
  git commit -m "提示信息"
  git push
  ```

- 新增已验证的规则：

  在相应文件夹下新建规则，然后更新到远程仓库

  ```shell
  git add 所有新建规则
  git commit -m "提示信息"
  git push
  ```

  ## 修改与删除规则

  由于只打算搞一个`master`，不弄其他分支，所以别弄版本回退了，修改与删除继续往后面走，提示信息里写上相应描述即可

