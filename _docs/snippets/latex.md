---
title: Latex
category: Snippets
---

> https://de.sharelatex.com/learn/Positioning_images_and_tables

### Basic images

```tex
\includegraphics[width=0.5\textwidth]{lion-logo}
```

### Basic positioning images

```tex
\usepackage[export]{adjustbox}

\includegraphics[width=0.5\textwidth, right]{lion-logo}
```

### Figure environment

```tex
\begin{figure}[h]
\includegraphics[width=0.5\textwidth, inner]{lion-logo}
\caption{Caption}
\label{fig:figure2}
\end{figure}
```

### Subfigure

```tex
\begin{figure}[h]
 
\begin{subfigure}{0.5\textwidth}
\includegraphics[width=0.9\linewidth, height=5cm]{lion-logo} 
\caption{Caption1}
\label{fig:subim1}
\end{subfigure}
\begin{subfigure}{0.5\textwidth}
\includegraphics[width=0.9\linewidth, height=5cm]{mesh}
\caption{Caption 2}
\label{fig:subim2}
\end{subfigure}
 
\caption{Caption for this figure with two images}
\label{fig:image2}
\end{figure}
```

### Wrapping text around a figure

```tex
\begin{wrapfigure}{l}{0.25\textwidth}
\includegraphics[width=0.9\linewidth]{lion-logo} 
\caption{Caption1}
\label{fig:subim1}
\end{wrapfigure}
```