# Introduction to Factorio

> *本项目仍在编辑中，也欢迎任何人从[github](https://github.com/tanganke/introduction-to-factorio)参与，进行pull request(PR)的提交([如何提交PR？](https://cloud.tencent.com/developer/article/1999727))，对git/github不熟悉的，可以[通过邮件联系我们](mailto:tang.anke@foxmail.com)。*

[在线文档](https://tanganke.github.io/introduction-to-factorio/)

## 项目结构

本项目基于[mdbook](https://hellowac.github.io/mdbook-doc-zh/zh-cn/index.html)，使用markdown文件格式，基本的markdown语法参考[Markdown语法文档](https://markdown.com.cn/basic-syntax/)。

```yaml
book.toml
src/            # 所有文本所在目录
    SUMMARY.md  # 本书的总目录
    ...
```

`src/SUMMARY.md` 定义了本书的整体目录结构，可以根据其找到具体要编辑的文件。

## 本地预览

1. 首先，克隆此仓库到本地，并进入项目根目录：

```bash
git clone https://github.com/tanganke/introduction-to-factorio/
cd introduction-to-factorio
```

2. 执行(*请确保已经正确安装 mdbook, 并将所在文件夹加入PATH环境变量*)：

```bash
mdbook serve
```

3. 打开浏览器，在地址栏输入 [`http://localhost:3000`](http://localhost:3000)
