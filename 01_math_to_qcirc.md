### 1. Basic Gates
These are list of primitive avaible in qiskit. Access them via ``QuantumCircuit``
| Gate | Description | simplify |
| :--- | :--- | :--- |
| XGate | $\sigma_x$ | bit flip|
| YGate | $\sigma_y$ | imaginary phase flip |
| ZGate | $\sigma_z$ | phase flip |

#### 1.1 XGate
It's mathematical representation below:
$$ 
M =
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
$$
Here's the code example:
```python
from qiskit.circuit.library import XGate
gate = XGate()
print(gate.to_matrix())             # X gate
print(gate.power(1/2).to_matrix())  # √X gate
print(gate.control(1).to_matrix())  # CX (controlled X)
```
Here's the result:
```text
[[0.+0.j 1.+0.j]
 [1.+0.j 0.+0.j]]
[[0.5+0.5j 0.5-0.5j]
 [0.5-0.5j 0.5+0.5j]]
[[1.+0.j 0.+0.j 0.+0.j 0.+0.j]
 [0.+0.j 0.+0.j 0.+0.j 1.+0.j]
 [0.+0.j 0.+0.j 1.+0.j 0.+0.j]
 [0.+0.j 1.+0.j 0.+0.j 0.+0.j]]
```
**NOTE:** As you can see, in qiskit we can replicate ``CXGate`` using ``XGate.control(1)``.
#### 1.2 YGate
#### 1.3 ZGate
#### 1.4 HGate