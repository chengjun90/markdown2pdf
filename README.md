# 从markdown到pdf

模板文件在markdown2pdf中。

- md是markdown文件，是笔记的内容
- book.ps1是powershell脚本，主要用来自动化编译LaTex
- metdata.yaml是标注pdf属性的文件
- template.tex是模板  
这个模板是从R语言包rticles中default.latex文件修改而来。这个文件也是从pandoc中的默认模板修改而来
- image是默认的插图文件夹

选中book.ps1文件，鼠标右击，选择“使用Powershell运行”，然后得到pdf文件。

更多描述见：[简单的笔记脚本：从markdown到pdf](https://zhuanlan.zhihu.com/p/31982147)

演示时运行环境：
- Win 10
- pandoc
- MiKTeX
