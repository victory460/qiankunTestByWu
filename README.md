node.js v8.11.4  
1104，主应用采用vue-cli脚手架，重新创建新的 demo

### 已解决
1，子应用与主应用，子应用与子应用跨域问题  
2，主应用改造为webpack vue 应用  
3，主应用 路由切换子应用  
4，子应用加载 qiankun 的生命周期  
5，子应用内部切换路由
6，部署
    -子应用部署可直接沿用以前的发布部署流程，没有什么要特殊处理的
    https://github.com/umijs/qiankun/issues/64  #[Bug]vue-cli3生产部署时发现的问题,并附带临时解决方法 #64
    -部署跨域，nginx 配置

#### master分支说明
主分支，各个分支问题解决合并到此分支

#### testRouter分支说明（已解决）
测试，解决 路由问题

#### testSubAppComponents分支说明
测试，解决 子应用组件问题

#### 待解决/待验证问题项
1，css污染问题.
	scoped（暂时解决方案）
2，JS变量隔离（待验证, qiankun已有，使用JS Sandbox）
3，子应用通信（待验证）
    使用本地存储，localStorage



	

## 拉取远程分支到本地
```sh
#情况一：目前本地还没拉代码，直接拉分支代码
git clone -b <branchName> https://github.com/wusp1994/qiankunTestByWu.git
#情况二：本地已经拉取了代码，想拉取远程某一分支的代码到本地
git checkout -b <branchName> origin/<branchName> #当前分支上创建一个分支，拉取远程到本地（方式一）
  # 如果报错 git fetch 同步仓库
git fetch origin <branchName>:<branchName>  #拉取远程分支到本地(方式二)
```