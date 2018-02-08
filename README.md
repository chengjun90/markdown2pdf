# 从markdown到pdf

模板文件在markdown2pdf中。

- md是markdown文件，是笔记的内容
- book.ps1是powershell脚本，主要用来自动化编译LaTeX
- metdata.yaml是标注pdf属性的文件
- template.tex是模板  
这个模板是从R语言包[rticles](https://cran.rstudio.com/web/packages/rticles/)中default.latex文件修改而来。[rticles](https://cran.rstudio.com/web/packages/rticles/)中的这个文件是从[pandoc](http://www.pandoc.org)中的默认模板修改而来
- image是默认的插图文件夹

选中book.ps1文件，鼠标右击，选择“使用Powershell运行”，然后得到pdf文件。

更多描述见：[简单的笔记脚本：从markdown到pdf](https://zhuanlan.zhihu.com/p/31982147)

演示时运行环境：
- Win 10
- pandoc
- TeX Live

```PowerShell
PS C:\Users\cheng> $PSVersionTable

Name                           Value
----                           -----
PSVersion                      5.1.16299.98
PSEdition                      Desktop
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0...}
BuildVersion                   10.0.16299.98
CLRVersion                     4.0.30319.42000
WSManStackVersion              3.0
PSRemotingProtocolVersion      2.3
SerializationVersion           1.1.0.1

PS C:\Users\cheng> xelatex --version
XeTeX 3.14159265-2.6-0.99998 (TeX Live 2017/W32TeX)
kpathsea version 6.2.3
Copyright 2017 SIL International, Jonathan Kew and Khaled Hosny.
There is NO warranty.  Redistribution of this software is
covered by the terms of both the XeTeX copyright and
the Lesser GNU General Public License.
For more information about these matters, see the file
named COPYING and the XeTeX source.
Primary author of XeTeX: Jonathan Kew.
Compiled with ICU version 58.2; using 58.2
Compiled with zlib version 1.2.11; using 1.2.11
Compiled with FreeType2 version 2.7.1; using 2.7.1
Compiled with Graphite2 version 1.3.9; using 1.3.9
Compiled with HarfBuzz version 1.4.6; using 1.4.6
Compiled with libpng version 1.6.29; using 1.6.29
Compiled with poppler version 0.52.0
Compiled with fontconfig version 2.12.1; using 2.12.1

PS C:\Users\cheng> pandoc --version
pandoc.exe 2.1.1
Compiled with pandoc-types 1.17.3, texmath 0.10.1, skylighting 0.6
Default user data directory: C:\Users\cheng\AppData\Roaming\pandoc
Copyright (C) 2006-2018 John MacFarlane
Web:  http://pandoc.org
This is free software; see the source for copying conditions.
There is no warranty, not even for merchantability or fitness
for a particular purpose.
```

PS1文件在PowerShell Core 6.0亦可运行。
```PowerShell
PS C:\Users\cheng> $PSVersionTable

Name                           Value
----                           -----
PSVersion                      6.0.0
PSEdition                      Core
GitCommitId                    v6.0.0
OS                             Microsoft Windows 10.0.16299
Platform                       Win32NT
PSCompatibleVersions           {1.0, 2.0, 3.0, 4.0...}
PSRemotingProtocolVersion      2.3
SerializationVersion           1.1.0.1
WSManStackVersion              3.0
```
