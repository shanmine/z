# z
Image CDN repository.

## 1. 搭建自己的图床

- 阿里OSS(推荐)
- 七牛云
- 腾讯云
- GitHub
- Gitee(现在不推荐了，问题比较多，防盗链、图裂等不稳定情况时有发生)

## 2. Git Log 格式输出

格式：`git log --pretty=format:"%h - %an[%ae], %C(yellow)%cd - %C()%s"`

    –pretty=format: 参数参考 https://git-scm.com/docs/pretty-formats：
    %h  ： commit id
    %an ：author name ，作者
    %ae ：author email ，作者 email
    %cd ：committer date (format respects --date= option) ，提交日期
    %cr ：committer date, relative ，提交日期，显示效果为 3天前、4个月前
    %ct ：committer date, UNIX timestamp ，提交日期，显示为 UTC 时间
    %cs ：committer date, short format (YYYY-MM-DD)
    %s  ：subject ，commit 信息
    %C(color​) ：设置颜色 ，可以指定某个信息的颜色，如设定 提交日期 %cd 的颜色 %C(yellow)%cd

示例：`git log --oneline --decorate --graph --all --pretty=format:"%h - %an[%ae], %C(yellow)%cd - %C(green)%s"`

