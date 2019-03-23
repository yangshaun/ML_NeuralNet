# NeuralNet

This project is basically for practicing NN.

## Data 
* [MNIST](http://yann.lecun.com/exdb/mnist/) - The handwritten digits

### Architecture
\begin{align}
 \textbf{input features}: \hspace{15pt} & x \in \mathbb{R}^D \\
 \textbf{linear}^{(1)}: \hspace{15pt} & u = W^{(1)}x + b^{(1)} \hspace{2em}, W^{(1)} \in \mathbb{R}^{M\times D} \text{ and } b^{(1)} \in \mathbb{R}^{M}  \label{linear_forward}\\
 \textbf{tanh}:\hspace{15pt} & h =\cfrac{2}{1+e^{-2u}}-1 \label{tanh_forward}\\
 \textbf{relu}: \hspace{15pt} & h = max\{0, u\} =
\begin{bmatrix}
\max\{0, u_1\}\\
\vdots \\
\max\{0, u_M\}\\
\end{bmatrix} \label{relu_forward}\\
 \textbf{linear}^{(2)}: \hspace{15pt} & a = W^{(2)}h + b^{(2)} \hspace{2em}, W^{(2)} \in \mathbb{R}^{K\times M} \text{ and } b^{(2)} \in \mathbb{R}^{K} \label{linear2_forward}\\
 \textbf{softmax}: \hspace{15pt} & z = \begin{bmatrix}
\cfrac{e^{a_1}}{\sum_{k} e^{a_{k}}}\\
\vdots \\
\cfrac{e^{a_K}}{\sum_{k} e^{a_{k}}} \\
\end{bmatrix}\\
 \textbf{predicted label}: \hspace{15pt} & \hat{y} = argmax_k z_k.
%& l = -\sum_{k} y_{k}\log{\hat{y_{k}}} \hspace{2em}, \vy \in \mathbb{R}^{k} \text{ and } y_k=1 \text{ if } \vx \text{ belongs to the } k' \text{-th class}.
\end{align}

