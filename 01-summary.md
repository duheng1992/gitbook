## 1、node环境安装

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;前端工程化开发，本地启动开发环境都是基于nodejs的，我们需要在检查一下自己的电脑上有没有开发环境，命令行运行node指令查看版本：`node -v`。

![1.png](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/fd0219645dd64ac5868f1b3d6b32c26d~tplv-k3u1fbpfcp-watermark.image?)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;由于这里使用的是纯净版的系统，没有安装任何环境，所以需要手动安装。这里给出node的官网安装地址: http://nodejs.cn/download/ .

官网界面如下：
![2.png](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/504cb9df698a4a4e815023594f113c75~tplv-k3u1fbpfcp-watermark.image?)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;我们可以根据自己的操作系统来选择，作者这里介绍平时最常用的两种系统：windows（以win11为例）和macOS（Big Sur11.4）的安装流程，非常的简单。

### 1.1、windows安装node
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;下载windows安装包后，双击安装文件即可进入安装环境，作者这里下载的是 node-v16.13.2-x64.msi的文件。

![3.png](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/86423df1ff514f51bb50d39c6e276e8e~tplv-k3u1fbpfcp-watermark.image?)
选择默认选项，一直Next即可，直到最后finish.

![4.png](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/e6729afc3ab64f0aa4462ef56e28d215~tplv-k3u1fbpfcp-watermark.image?)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;由于windows的安装包会自动配置环境变量，所以这里你不需要其他额外的配置。再次运行 `node -v`查看：

![5.png](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/5dc25a9c8bdb4d0baf9775efcf15cd27~tplv-k3u1fbpfcp-watermark.image?)

安装成功！！

### 1.2、macOS安装node
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;下载macOS安装包，这里作者下载的是node-v16.13.2.pkg文件，双击即可进入安装弹窗：

![6.png](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/ff1acfd84a5342fbb6a020bc3d67671c~tplv-k3u1fbpfcp-watermark.image?)
一直继续下一步，知道最后安装成功：

![7.png](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/1265e7a221b94dd6a06f2037bfc5860b~tplv-k3u1fbpfcp-watermark.image?)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;最后的界面告诉你了node的安装环境的目录位置：`/usr/local/bin/node`，说明mac也会自动加入环境变量，也无需自己额外配置。接下来查看node版本：

![8.png](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/63c199f8650241cb8edc062e81b11328~tplv-k3u1fbpfcp-watermark.image?)

mac下也安装成功！！

## 2、开发工具准备
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;前端的开发工具，常见的有vsCode、webStorm、atom等，只需用其中之一便足可以完成您的开发任务。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;vsCode作为目前最为流行的轻量级开发工具，广受前后端程序员的喜爱，其插件库也是十分的丰富，可以供开发的进行自定义配置，而且提供了插件开发的功能，使得开源作者能够更加轻松的自定义自己的插件，并且有支持远程开发等优点。相比于webStorm和sublime这种需要购买正式版（sublime虽然不买也没什么关系）的产品，其最直接的优点是他是免费的！
vsCode官网地址为：`https://code.visualstudio.com/`，开发者可以下载自己所需的版本：

![image.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/530390cbd5994d47a613849acbeb5f40~tplv-k3u1fbpfcp-watermark.image?)
国内用户未翻墙的可能会出现下载缓慢的问题，这里作者提前下载好了国内版本放在文章末尾供大家下载。

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;atom也是免费的开发工具，这个根据自己的喜好来使用。作者一开始写网页也是用的atom，但是当你下载了官网的安装包，看到他的大小后，或者在使用很长一段时间后打开资源管理器后，你可能就会像作者一样弃用它！这里还是给出其官网地址`https://atom.io/`，他的界面作者还是挺喜欢的。

## 3、react项目开发环境搭建
react工程化项目创建的脚手架工具这里作者介绍主流的两种：`create-react-app`和`vite`.
### 3.1、create-react-app构建
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;这里使用npx安装：`npx create-react-app <工程名>`。
注意工程名称使用字母数字连接线的形式(范例参考：<https://create-react-app.dev/docs/getting-started/>)，这里作者使用hello-world1.
构建成功后会看到控制台打印如下指令：

![10.png](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/1432f5a2ae64472f808a67b4c2f6f3e9~tplv-k3u1fbpfcp-watermark.image?)

进入工程根目录`cd ./hello-world1`
> 若创建时没有安装依赖成功，进入工程根目录下手动安装`npm inatall`即可

执行指令：`npm start`，启动成功后在浏览器输入网址`localhost:3000`即可看到欢迎界面：

![11.png](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/15f0d1758e074de2b5f06d2541eb3096~tplv-k3u1fbpfcp-watermark.image?)

### 3.2、vite构建
终端输入指令
```sh
# npm 6.x
npm init vite@latest <工程名> --template <模板名>
# npm 7+
npm init vite@latest <工程名> -- --template <模板名>
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;这里我们当然使用`react`作为模板名、hello-world2作为工程名来构建工程目录。输入指令后你会发现项目构建的很快，那是因为脚手架没有默认帮你安装依赖，所以要进入工程目录（`cd ./hello-world2`）并手动安装依赖：`npm install`。依赖安装完成后，即可启动项目：`npm run dev`，同样的，在浏览器输入网址`localhost:3000`即可看到欢迎界面：

![12.png](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/a5430aec68b34e5eb9e34f87813d8ff3~tplv-k3u1fbpfcp-watermark.image?)

至此项目就启动完毕了~~ <br><br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;如果您只是想快速开发一个项目，环境配置到这里就结束了。以下内容为选择性观看内容，如果您觉得依赖安装比较慢，又或者需要管理不同版本的node，可以继续往下看。

## 4、依赖安装的方式(选读)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;上边章节中，作者主要使用`npm install`的方式安装依赖，但是有时候，尤其是网络不太好的情况下，依赖总是不能被正确安装，出现安装错误。这个时候可能就需要进行下一步操作。
### 4.1、npm国内镜像配置
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;国内npm镜像可以绕开被墙的困扰，作者推荐taobao的镜像。你可以这样执行命令：
`npm install -g cnpm --registry=https://registry.npm.taobao.org`，这样就全局安装了使用的taobao国内镜像的cnpm指令。你在项目根目录下试试`cnpm install`就会快很多。<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;你还可以这样配置镜像：
`npm config set registry https://registry.npm.taobao.org`，这样你即使使用npm指令安装，也会走国内镜像安装。

### 4.2、不同的依赖安装策略
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;前端工程化项目依赖安装不只有npm方式，还有他的各种变种。比如安装速度快，版本能够更好统一的`yarn`或者运行速度更快的`pnpm`。细心的读者可以发现，上面`create-react-app`安装的方式使用了`npx`，而没有使用`npm -g`这种全局指令方式。在`npm 5.2`以后的版本默认会安装`npx`命令，它可以避免全局安装模块。这些不同的策略在之后的文章中会提及，在这里不做过多的赘述。

### 4.3、使用nvm管理node版本
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;nvm是目前比较主流的node版本管理工具，类似的还有nodist（`https://github.com/nullivex/nodist/releases`）。这里以nvm为准进行介绍。
#### 4.3.1、windows环境安装
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;进入官网下载链接`https://github.com/coreybutler/nvm-windows/releases`，下载assets中的安装包（文章末尾提供安装包）。

![13.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/e9f85431174642a19e5a24e620c70527~tplv-k3u1fbpfcp-watermark.image?)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;这里可以直接下载setup版的，解压后双击就可安装。当然也可以选择noinstall版本的，通过手动配置环境来达到相同的目的。这里以安装版为例。下图为安装界面：

![14.png](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/e0509c826a9248e79ba080c4c10a3d61~tplv-k3u1fbpfcp-watermark.image?)
一路next到底完成安装即可。环境变量已经自动配置好了。
在命令行中检查是否安装成功：

![15.png](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/f74a35a040244113a5f4594e6e6631d9~tplv-k3u1fbpfcp-watermark.image?)
看到版本说明已经正确安装！！
#### 4.3.2、MacOS环境安装（需翻墙）
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;进入官网下载链接`https://github.com/nvm-sh/nvm#installing-and-updating`，可以看到安装指引，我们遵从官方给的指令直接执行即可：
```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```
接下来您可能不会看到安装成功，反而会提示如下：
> Failed to connect to raw.githubusercontent.com port 443

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;这是因为某种神秘的东方力量导致的github访问的问题，我们可以借助网址`https://ipaddress.com/website/raw.githubusercontent.com`查一下`githubusercontent.com`的真实IP，输入githubusercontent.com查询会看到：

![16.png](https://p9-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/9bcc81ba9906410883cdc36ebc6c567c~tplv-k3u1fbpfcp-watermark.image?)
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;我们找下边查到的IP其中一个即可（如果不行就换着试试），执行下述步骤：

1. 进入mac的host文件：`sudo vim /etc/hosts`
2. 最下边追加IP映射

![17.png](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/1313dfeb43ef43ffbe95af3a7404efc9~tplv-k3u1fbpfcp-watermark.image?)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;经过这两步后再次尝试一哈，就可以执行成功了。
```sh
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;如果很不幸你叒叕出现了如下错误，不要惊慌，应该是没有检测到你的github账户，你只需要打开github主页登录账号重试即可。
> unable to access 'https://github.com/nvm-sh/nvm.git/': LibreSSL SSL_connect: SSL_ERROR_SYSCALL in connection to github.com:443

最后！<br>

安装成功的界面如下：

![18.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/4c079e6e5622482eba29ed5a0a1d17be~tplv-k3u1fbpfcp-watermark.image?)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;此时先不要着急，全局的`nvm`指令还没有加入环境变量中，需要你来手动添加。执行命令(以zsh终端为例) `sudo vim ~/.zshrc`，进入编辑后，追加：
```sh
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```
然后生效配置文件：`source ~/.zshrc`即可。

现在就试试nvm指令：

![19.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/eaf9cf52f5de4de6a9e0cb7298be3925~tplv-k3u1fbpfcp-watermark.image?)

成功！

### 4.3.3、nvm基础使用

我们可以使用`nvm list`命令查看当前node的版本列表

![20.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/d6581cddd355448681074dbd60bc7e11~tplv-k3u1fbpfcp-watermark.image?)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;可以看到，当前只有系统默认的16.13.2版本。如果想要安装别的node版本，没有必要再去node官网下载了，可以直接使用nvm指令下载。我们可以先使用`nvm ls-remote`看一下官方都有哪些正式版本：

![21.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/6cd2487b259d409fbf8a3cc5023710c4~tplv-k3u1fbpfcp-watermark.image?)

列出的版本都是可以安装的，我们这里可以安装稳定版：`nvm install stable`

![23.png](https://p6-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/9d7eed274a1a4381b85577cc586b9a3d~tplv-k3u1fbpfcp-watermark.image?)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;可以看到截止作者写这篇文章时，node的稳定版本是17.4.0，nvm会自动切换进安装的版本上。如果想要自定义版本号安装，可以使用指令`nvm install <版本号>`

![24.png](https://p1-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/03f3766934de45d18102e710c4aa4ff3~tplv-k3u1fbpfcp-watermark.image?)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;这里我们安装了12.22.10版本，再次`nvm list`可以看到已经有三个版本了。想要在多个版本之间切换，只需使用指令`nvm use <版本号>`即可一键切换！

![25.png](https://p3-juejin.byteimg.com/tos-cn-i-k3u1fbpfcp/d6c5464fa34b4448b6df8505a92c64e7~tplv-k3u1fbpfcp-watermark.image?)


至此，前端工程化项目的环境配置已经结束！ 

## 5、附件
附件清单：vscode安装包、nvm安装包（win）、atom安装包（mac）。<br>
下载链接：
> 链接: https://pan.baidu.com/s/1zD2s9UjXrVZ06NANnx8oXg  提取码: 5diu
