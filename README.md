
1. ### Use proper indentation.

```latex
\begin{frame}[t]{Functions} \vspace{4pt}

    \begin{block}{Definition of a Function}
        A function is a rule that assign to each element $x$ in a set $D$ exactly one element, called $f(x)$, in a set $E$.
    \end{block} \vspace{10pt}

\end{frame}
```

2. ### Give horizontal linebreak for nested command and `if else` like control flow.

```latex
Set $D$ is called the \only<1>{\line(1,0){50}}
                      \only<2>{
                           \textcolor{magenta}{domain}
                      }
                      \, of the function.\\[10pt]

Set $E$ is called the \only<1>{\line(1,0){50}}
                      \only<2>{
                            \textcolor{magenta}{range}
                      }
                      \, of the function.
```

3. ### Keep column in different indented block so that different columns can be differentiated

```latex
\begin{columns}[onlytextwidth]
        
    \column{.4\textwidth}
    $\sqrt{x^2} = $ \vspace{10pt}
    \begin{enumerate}[(A)]
        \item $x$
        \item $-x$
        \item $|x|$
        \item undefined
    \end{enumerate}
                                            \column{.6\textwidth}
                                            \only<3>{
                                                $\sqrt{x^2}=
                                                            \begin{cases}
                                                                -x, & x<0\\
                                                                x,  & x\geq 0
                                                            \end{cases}
                                                $
                                            }\\[10pt]
                                            \only<2->{
                                                    \includegraphics[scale=.19]{absolute}
                                            }
\end{columns}
```

4. ### Do not use extension of filename to reduce characers taken and increase readability.

```latex
\includegraphics[scale=.19]{absolute}
```

5. ### Keep images in separate directory like `Images`. If we use `\graphicspath{{./Images/}}`, we need not to specify full image address in `\includegraphics`.

```latex
\graphicspath{{./Images/}}
\includegraphics[scale=.18]{WordRepresentationOfWord2Vec}
```

6. ### For bibliography, maintain bibliography database file

```latex
\bibliography{citations.bib}
\bibliographystyle{plain}
```

7. ### Use proper identifiable, readable, recallable name for citation entry

```latex
@inproceedings{MultiplexHeterogeneousGraphConvolutionalNetwork,
  title={Multiplex Heterogeneous Graph Convolutional Network},
  author={Yu, Pengyang and Fu, Chaofan and Yu, Yanwei and Huang, Chao and Zhao, Zhongying and Dong, Junyu},
  booktitle={Proceedings of the 28th ACM SIGKDD Conference on Knowledge Discovery and Data Mining},
  pages={2377--2387},
  year={2022}
} 
```

8. s### We can structure a latex project like following way. Main project is segregated in different parts. The parts are then included in `main.tex` file.

```
.
├───Images
│   ├───image1.png
│   └───image2.png
├───main.tex
├───introduction.tex
├───body.tex
└───conclusion.tex
```

`main.tex:`
```latex
...
\graphicspath{{./Images/}}
...
\include{introduction}
\include{body}
\include{conclusion}
...
```