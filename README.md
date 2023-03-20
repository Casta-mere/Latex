# Latex
My Latex


# Tips

## 等宽字体

    \texttt{123456}

## 修改局部字体/字号/间距

    \usepackage{fontspec}
    \usepackage{xeCJK}
    \setCJKmainfont{Microsoft YaHei}

    \newcommand{\cvsection}[1] {
	\vspace{14pt}
	\cvtext{
        % 使用 group 在内部修改间距等
        \begingroup
        \renewcommand{\CJKglue}{\hskip 2.5pt} %修改行距
		\textbf{\LARGE{\textcolor{darkcol}{\uppercase{#1}}}}\\[-4pt]
		\textcolor{maincol}{ \rule{0.1\textwidth}{2pt} } \\
        \endgroup
        }
    }

## 空格
|   代码   |  长度  |
| :------: | :----: |
|    \\,    | 3/18em |
| \enspace | 0.5em  |
|  \quad   |  1em   |
|  \qquad  |  2em   |

## 连写

    LaTeX 排版以及正规排版中，如果你输入 ff、fl、fi、ffi 等内容，它们会默认连写。在字母中间插入空白的箱子以强制不连写，比如 f\mbox{}。

## 行内右对齐

    \hfill 内容

## 特殊符号

    $\%$ --- %

## 表格修改列高

在\\后加入高度，如

    \begin{tabular*}{1\mpwidth}{p{0.69\mpwidth}  r}
        \textcolor{darkcol}{\textbf{#3}} & \\[7pt]
        \textcolor{darkcol}{\textbf{#4}} & \\[7pt]
    \end{tabular*}\\