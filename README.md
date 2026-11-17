# Portable dotfiles

适合在临时使用的电脑上手打的 Bash 和 Vim 最小配置，无需安装插件。

将 `.bashrc`、`.inputrc` 和 `.vimrc` 的内容合并到主目录中的同名文件，保留已有配置。`.inputrc` 中的 `$include /etc/inputrc` 用于加载系统默认设置，已有这行时无需重复添加。

让当前 Bash 生效：

```bash
source ~/.bashrc
bind -f ~/.inputrc
```

Vim 重新打开即可。登录 Bash（例如 macOS）需确保 `~/.bash_profile` 加载 `.bashrc`：

```bash
[ -f ~/.bashrc ] && . ~/.bashrc
```

Tab 循环选择补全候选；输入命令前缀后按上下方向键，搜索匹配的历史记录。Git 等命令的参数补全需要系统另有 `bash-completion`。

`n` 调用 Vim，`l` / `la` / `ll` 使用系统自带的 `ls`。Vim 启用相对行号、四空格缩进、当前行列高亮，并显示 Tab 和行尾空格。
