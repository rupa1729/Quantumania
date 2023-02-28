# Quantumania

### Inspiration:
- Quantum chemistry  has helped to advance other areas of science and technology. For example, it has been used to design new drugs, develop more efficient catalysts for industrial processes, and understand the properties of materials used in electronic devices [^1]

- The limiting factor of Classical models is you have to pick a certain area where you have to compromise on accuracy to stay within the computational limit. Each simplification  reduces the overall accuracy  of your model. "The coarser your data , the more labor intensive your lab work"[^2] 

- Now even in the NISQ era of Quantum computer , we have quantum algos such as VQE[^3]  which has ability to speed up optimization problems and efficient simulations of complex molecules.We intend to go more deeper into this problem

- As a part of Quantum Chemistry Challenge[^4], we  tried to tackle the ground state problem of BeH2 molecule  

### What it does?
- AS a part of this hackathon we have calculated, ground state energy of BeH2 molecule. For this task we have taken use of quantum algorithms and quantum error mitigation to get the energy as accurate as possible. 
- Quantum error mitigation is the way to mitigate the error while working in noisy quantum computer. Our code is efficient to calculate the error mitigated ground state energy of BeH2 molecule. 
- Also, our code is flexible enough, if we want to change optimization technique and error mitigation technique very easily. 
- We used qiskit runtime service for error mitigation and build a module to calculate accurate ground state energy

### How we build it?
#### Calculation of ground state energy:
- We compute the ground state energy for the **BeH2 molecule at an interatomic distance 1.33 Angstroms**. 
- The number of **qubits is reduced to 6** by using the **Entanglement forging technique**. 
- The ansatz are constructed using RealAmplitude from Qiskit with linear entanglement layers. The initial parameters are chosen randomly. The energy is minimized using the COBLYA optimizer.
- **Error -mitigation:**
- In our module, user will give backend names (if it is local simulator or real backend) if they give local simulator they need to specify the noise model, problem created from previous part, optimizer, res_level ( which mitigation technique), opt_level(optimization level) , initial point. with this our module will calculate the ground state energy of BeH2 molcule

#### Result:
**VQE_Entanglement forging = -15.547195514957645 Hatree**

**Exact_NumpySolver = -15.595117562573 Hatree**

### Team name: Quantumfeed
### Team members
Ashwini Kannan , Indranil Maiti, Nadeem khan, , Sairupa Thota  

### References
[^1]: https://arxiv.org/abs/1808.10402
[^2]: https://www.scientificamerican.com/article/how-quantum-computing-could-remake-chemistry/
[^3]: https://arxiv.org/abs/2107.12705
[^4]: https://arxiv.org/abs/1704.05018
[^5]: https://github.com/Qiskit-Extensions/circuit-knitting-toolbox

