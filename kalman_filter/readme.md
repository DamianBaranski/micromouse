Wektor stanu: 
```math
\begin{align*} x_k = \begin{bmatrix} x \ y \ \theta \ v_x \ v_y \ v_{\theta} \ b_g \end{bmatrix} \end{align*}
```
Równania stanu:
```math
 \begin{align*} x_{k} = A x_{k-1} + B u_{k-1} + w_{k-1} \end{align*}
```
Macierz A: 
```math 
\begin{align*} A = \begin{bmatrix} 1 & 0 & -v_{\theta} \Delta t \sin(\theta) & \Delta t \cos(\theta) & 0 & 0 & 0 \\ 0 & 1 & v_{\theta} \Delta t \cos(\theta) & \Delta t \sin(\theta) & 0 & 0 & 0 \\ 0 & 0 & 1 & 0 & 0 & \Delta t & 0 \\ 0 & 0 & 0 & 1 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & 1 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 & 1 & 0 \\ 0 & 0 & 0 & 0 & 0 & 0 & 1 \end{bmatrix} \end{align*}
```

Macierz B: 
```math
\begin{align*} B = \begin{bmatrix} \frac{1}{2} \Delta t^2 \cos(\theta) & \frac{1}{2} \Delta t^2 \cos(\theta) \\ \frac{1}{2} \Delta t^2 \sin(\theta) & \frac{1}{2} \Delta t^2 \sin(\theta) \\ 0 & 0 \\ \Delta t \cos(\theta) & \Delta t \cos(\theta) \\ \Delta t \sin(\theta) & \Delta t \sin(\theta) \\ 0 & 0 \\ 0 & 0 \end{bmatrix} \end{align*}
```
Wektor szumu procesowego: 
```math
\begin{align*} w_k \sim N(0, Q) \end{align*}
```

Macierz szumu procesowego:
```math
\begin{align*} Q = \begin{bmatrix} \sigma_x^2 & 0 & 0 & 0 & 0 & 0 & 0 \\ 0 & \sigma_y^2 & 0 & 0 & 0 & 0 & 0 \\ 0 & 0 & \sigma_{\theta}^2 & 0 & 0 & 0 & 0 \\ 0 & 0 & 0 & \sigma_{v_x}^2 & 0 & 0 & 0 \\ 0 & 0 & 0 & 0 & \sigma_{v_y}^2 & 0 & 0 \\ 0 & 0 & 0 & 0 & 0 & \sigma_{v_{\theta}}^2 & 0 \\ 0 & 0 & 0 & 0 & 0 & 0 & \sigma_{gyro}^2 \end{bmatrix} \end{align*}
```
Równania pomiarowe: 
```math
\begin{align*} z_k = H x_k + v_k \end{align*}
```
