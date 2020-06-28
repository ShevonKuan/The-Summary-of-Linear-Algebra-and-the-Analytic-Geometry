# 线性代数与解析几何笔记
#### Shevon Kuan
## 简介

这是我基于 Latex2$\varepsilon$ 的数学笔记,它是一个系列并将使用一致的模板(目前仅部分开源),将来我可能会对该模板作独立开源处理.这个笔记基于华南理工大学的线性代数课本进行总结.目前由于期末考前只完成了笔者最需要复习的部分,剩余部分仍未完工,并且目前暂不考虑完工,有意加入并希望帮忙完善的的请发邮件[联系我][contact]

[contact]: mailto:331749486@qq.com

**Demo:**
![element](https://github.com/ShevonKuan/Probability-and-Mathematical-Statistics/raw/master/readme_image/main.png)


----

## 编译介绍
```Latex``` 编译链```XeLaTex -> bibtex -> makeindex -> texindy -> xeLaTex重复编译```对应```VS Code```设置如下:
```json
"latex-workshop.latex.recipes": [
    {
        "name": "完整编译链",
        "tools": [
            "xelatex",
            "bibtex",
            "makeindex",
            "texindy",
            "xelatex",
            "xelatex"
        ]
    },
]
```
各命令具体配置如下：
```json
"latex-workshop.latex.tools": [
    {
        // 编译工具和命令
        "name": "xelatex",
        "command": "xelatex",
        "args": [
            "-synctex=1",
            "-interaction=nonstopmode",
            "%DOCFILE%"
        ]
    },
    {
        "name": "bibtex",
        "command": "bibtex",
        "args": [
            "%DOCFILE%"
        ]
    },
    {
        "name": "texindy",
        "command": "texindy",
        "args": [
            "%DOCFILE%.idx"
        ]
    },
    {
        "name": "makeindex",
        "command": "makeindex",
        "args": [
            "%DOCFILE%.nlo",
            "-s",
            "nomencl.ist",
            "-o",
            "%DOCFILE%.nls"
        ]
    }
],
```
----
## TODO:
目前不打算继续完善.

