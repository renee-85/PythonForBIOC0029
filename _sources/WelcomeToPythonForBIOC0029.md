# Welcome to Python for BIOC0029

All techniques we use produce data that need to be analyzed. Some instruments come with their own vendor-specific, often licensed, software for data acquisition and analysis. These programs usually have a black-box interface so we cannot control equations and / or parameters. That is why we prefer to work with data analysis software or programming languages that allow us flexibility.

There are many options out there: Wolfram Mathematica, MathWorks MATLAB, Microsoft Excel with Solver add-in, Maple, R Studio, WaveMetrics IGOR Pro, GraphPad (Prism), SigmaPlot, Origin, … and __Python__!

```{image} ./SoftwarePackagesProgrammingLanguages.png
:alt: Software Packages and Programming Languages
:width: 600px
:align: center
```

Python is a programming language that can be used to analyse biophysical and biochemical data, to analyse protein/DNA/RNA sequences, to process images, to build mathematical models of biochemical systems, to perform biomolecular simulations ...

These notes introduce Python Jupyter Notebooks to biochemists. We focus on biophysical and biochemical data analysis.



## __<font color=blue>Why Python?</font>__
---

- Python is developed under __an open source license__, which makes it _free to use and distribute_. Its development is _driven by the community_.

- It is __a high-level programming language__, written in a form that is close to our human language. It makes is _easier for the programmer to write, modify, and debug_ the code.

- It is __portable__: _the same source code works in different environments_ (_e.g._ operating systems).

- Python provides __extensive libraries__. Many __high-use programming tasks__ have already been scripted into these libraries which reduces length of code to be written significantly. Examples include _NumPy, pandas, matplotlib, and SciPy_.

```{image} ./NumPySciPyPandasMatplotlib.png
:alt: NumPy, SciPy, pandas, and matplotlib
:width: 600px
:align: center
```

- The wide base of users and active developers has resulted in __a rich online support (documentation and forums)__ to encourage development and the continued adoption of the language. _Google it!_

- Alternatively, use __AI code assistant tools__, like ChatGPT API, GitHub Copilot, Replit Ghostwriter, or Amazon CodeWhisperer, to help you write your code. _But be aware, sometimes, AI assistants do not give what you need: always read and understand the code they suggest!_



## __<font color=blue>Why Jupyter Notebooks?</font>__
---

Jupyter notebooks (__.ipynb files__) are __a presentation layer__. They allow us to create and share documents that contain __cells__. There are three types of cell:
- live __code__
- explanatory text, equations, tables, and figures using __Markdown__
- output in __Raw NBConverter__.

Each Jupyter notebook uses __a kernel__. The kernel runs our code cells in a specific programming language, in our case, Python. Any output is displayed. The kernel's state persists over time and between cells. For example, if a library has been imported in one cell, then that library will be available for the whole notebook. We can reset the kernel by restarting it.

In code cells, lines with __`#`__ are __comment__ lines. They are not evaluated. Comments are used to explain what the code is doing.



### __<font color=red>Markdown</font>__
---

Markdown is a language that makes it very easy to write formatted content. It uses very easy-to-remember syntax. The following cheat sheet can help when writing explantory text, equations, and tables in Markdown cells:

```{image} ./MarkdownCheatSheet.png
:alt: A Markdown Cheat Sheet
:width: 600px
:align: center
```