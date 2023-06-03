
### Use proper indentation.

```latex
\begin{frame}[t]{Functions} \vspace{4pt}

    \begin{block}{Definition of a Function}
        A function is a rule that assign to each element $x$ in a set $D$ exactly one element, called $f(x)$, in a set $E$.
    \end{block} \vspace{10pt}

\end{frame}
```

### Give horizontal linebreak for nested command and `if else` like control flow.

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

### Keep column in different indented block so that different columns can be differentiated

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

### Do not use extension of filename to reduce characers taken and increase readability.

```latex
\includegraphics[scale=.19]{absolute}
```