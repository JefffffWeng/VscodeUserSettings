# VSCode 用户设置说明

本文件用于记录当前VSCode工作区的个性化配置，主要针对Python开发环境进行优化。

## 通用设置

### 界面主题
```json
"workbench.colorTheme": "Atom One Dark"
```
- 使用Atom One Dark暗色主题，提供舒适的代码高亮效果

### 编辑器设置
```json
"editor.fontFamily": "JetBrains Mono, Consolas, 'Courier New', monospace",
"editor.rulers": [120]
```
- 字体使用JetBrains Mono等宽字体族
- 120字符标尺线帮助保持代码规范

## Python专项配置

### 保存时自动格式化
```json
"[python]": {
    "editor.codeActionsOnSave": {
        "source.organizeImports": "explicit"
    },
    "editor.defaultFormatter": "ms-python.python",
    "editor.formatOnSave": true
}
```
- 保存时自动整理import语句
- 启用自动格式化功能

### 代码格式化工具链
```json
"black-formatter.args": ["--line-length", "120"],
"python.formatting.provider": "black",
"python.sortImports.path": "isort",
"python.sortImports.args": ["--profile", "black"]
```
- 使用Black作为主要格式化工具
- 行长度限制为120字符
- 配合isort进行import语句排序
- 配置isort与Black的格式兼容

## 推荐扩展
1. Python (ms-python.python)
2. Black Formatter (ms-python.black-formatter)
3. Atom One Dark Theme (akamud.vscode-theme-onedark)
