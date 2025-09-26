<font face="Arial" size="4" color="black">
  
# Creation-of-Multipartite-Entangled-GHZ-and-W-States
GHZ and W-states using the QuTip

GHZ and W-states have been used as resources for various quantum information processing tasks, such as quantum teleportation, quantum cryptography, and quantum error correction.

*Entangled systems* form the basis of all *quantum computers* [1]. Different types of entanglement can exist in multipartite quantum systems. The type of entanglement refers to the specific way in which the qubits are correlated and entangled with each other. *Bipartite entanglement* is the simplest type of entanglement, involving only two qubits or two subsystems. Examples include *the Bell states* and *EPR pairs*. EPR pairs can be in any of the Bell states or other entangled states. Genuine multipartite entanglement involves more than two qubits, and all the qubits are entangled with each other. Examples include *the Greenberger-Horne-Zeilinger (GHZ) states* and the *W-states*. In *the partial entanglement*, only a subset of qubits in the system is entangled, while the others may be in a separable state or entangled with other subsets. Examples include states like |00⟩|+⟩, where the first two qubits are entangled, but the third qubit is in a separable state. *Cluster state entanglement* is a specific type of multipartite entangled state that exhibits a lattice-like structure of entanglement. These states are highly entangled and are used as resources for certain quantum computing models, such as *measurement-based quantum computing*. *Graph state entanglement* is another class of multipartite entangled states that are defined based on a graph structure. Each qubit in a graph state is associated with a vertex of the graph, and entanglement exists between qubits connected by edges. Graph states have applications in quantum error correction and quantum communication protocols.

The most prominent representatives are defined as follows:
1. Bell-states:
   <div align="center">
    <img src="images/Bell_states.png">
   </div>

The Bell states are maximally entangled states, meaning that the two qubits are correlated in such a way that measuring one qubit instantly determines the state of the other qubit, regardless of the distance between them.

2. The Greenberger-Horne-Zeilinger (GHZ) states are a class of entangled states that involve three or more qubits [2]. The general form of an n-qubit GHZ state is:

   <div align="center">
    <img src="images/GHZ_general.png">
   </div>

In this formula:

<div align="center">
    <img src="images/GHZ_general2.png">
   </div>

represents the tensor product of n qubits, all in the state ∣0⟩ and

<div align="center">
    <img src="images/GHZ_general3.png">
   </div>

represents the tensor product of n qubits, all in the state ∣1⟩.

For example, the three-qubit GHZ state is:

<div align="center">
    <img src="images/GHZ3.png">
   </div>

And the four-qubit GHZ state is:

<div align="center">
    <img src="images/GHZ4.png">
   </div>

GHZ states are highly entangled states that exhibit non-local correlations among the qubits. They have been utilized in various quantum information processing tasks, including quantum error correction, quantum secret sharing, and testing the foundations of quantum mechanics.

3. W-states are another class of entangled states that involve three or more qubits [3]. The general form of an n-qubit W state is:

   <div align="center">
    <img src="images/W_state.png">
   </div>

In this formula, each term in the superposition has exactly one qubit in the state ∣1⟩, while all other qubits are in the state ∣0⟩. The number of terms in the superposition is equal to the number of qubits, n.
For example, the three-qubit W state is:

<div align="center">
    <img src="images/W3.png">
   </div>

And the four-qubit W state is:

<div align="center">
    <img src="images/W4.png">
   </div>

W-states are highly entangled and have the property that if one qubit is measured in the state ∣1⟩, the remaining qubits will be left in the state ∣0⟩, while if one qubit is measured in the state ∣0⟩, the remaining qubits will be left in a W-state of one fewer qubit. W-states are more robust against particle loss. If one qubit is lost, the entanglement between the remaining qubits persists.
The Bell states can be seen as special cases of GHZ and W states for two qubits. The Bell state ∣ψ+⟩ is a 2-qubit GHZ state. The Bell state ∣ϕ+⟩ is a 2-qubit W state. The other two Bell states, ∣ψ−⟩ and ∣ϕ−⟩, are not directly equivalent to GHZ or W states, but they are still maximally entangled states and share many of the same properties as GHZ and W states.

There are two Jupyter Notebooks here:

1. Bipartite_entanglement: https://github.com/AnaKhromova/Creation-of-Multipartite-Entangled-GHZ-and-W-States/blob/main/bipartite_entanglement.ipynb. This notebook includes the codes and theory for Bipartite Entangled States Preparation Theory, with QuTiP examples where it is explained how we prepare *the Bell states*, and the Two-Qubit Entangled State Preparation in Trapped Ions, with QuTiP examples, where we explain how we prepare the Bell state experimentally using the trapped ion with the visualizations on the Bloch sphere.
2. Multipartite Entangled States Preparation, with QuTiP examples, is explained in the Jupyter Notebook https://github.com/AnaKhromova/Creation-of-Multipartite-Entangled-GHZ-and-W-States/blob/main/multipartite_entanglement.ipynb. Here, we present the preparation of the GHZ and W-states. For the creation of the W-states, we will elaborate on a recursive algorithm.

# References

[1] D. Bruss and G. Leuchs, Lectures on quantum information, (Wiley-VCH, Weinheim) (2007), 337.

[2] D.M. Greenberger, M.A. Horne, A. Shimony, A. Zeilinger, "Bell theorem without inequalities", Am. J. Phys. 58(12), pp. 1131–1143 (1990)

[3] W. Dür; G. Vidal & J. I. Cirac (2000). "Three qubits can be entangled in two inequivalent ways". Phys. Rev. A., 62 (6): 062314. arXiv:quant-ph/0005115

[4] Anastasiya Khromova, Quantum gates with trapped ions using magnetic gradient induced coupling, PhD Thesis 2012, https://dspace.ub.uni-siegen.de/entities/publication/cd2a16e9-ba44-4610-bd17-4066af655b7e

[5] Efficient quantum algorithms for GHZ and W states, and implementation on the IBM quantum computer, Diogo Cruz et al., https://arxiv.org/pdf/1807.05572

[6] Open Quantum Assembly Language, Andrew W. Cross, Lev S. Bishop, John A. Smolin, Jay M. Gambetta, https://arxiv.org/abs/1707.03429

[7] How to implement a circuit preparing the three-qubit W state?, https://quantumcomputing.stackexchange.com/questions/15506/how-to-implement-a-circuit-preparing-the-three-qubit-w-state

[8] Experimental entanglement of four particles by C. A. Sackett et al. (2000), https://www.rle.mit.edu/cua_pub/8.422/Reading%20Material/QC-sackett-wineland-et-al-experimental-entanglement-of-four-particles-nature-v404-p256-16mar00.pdf

[9] Scalable multiparticle entanglement of trapped ions by H. Häffner et al. (2005), https://arxiv.org/pdf/quant-ph/0603217

[10] Experimental demonstration of five-photon entanglement and open-destination teleportation by Z. Zhao et al. (2004), https://arxiv.org/pdf/quant-ph/0402096

[11] Experimental realization of a three-qubit entangled W-state by M. Eibl et al. (2004), https://www.researchgate.net/publication/6628945_Experimental_Realization_of_a_Three-Qubit_Entangled_W_State

[12] Preparation and measurement of three-qubit entanglement in a superconducting circuit by L. DiCarlo et al. (2010), https://www.researchgate.net/publication/46821151_Preparation_and_Measurement_of_Three-Qubit_Entanglement_in_a_Superconducting_Circuit

[13] Generation of three-qubit entangled states using superconducting phase qubits by M. Neeley et al. (2010), https://arxiv.org/abs/1004.4246

QuTip manuals used:

[1] Measurement of Quantum Objects, https://qutip.readthedocs.io/en/latest/guide/guide-measurement.html#obtaining-measurement-statistics-observable

[2] Plotting on the Bloch Sphere, https://qutip.readthedocs.io/en/latest/guide/guide-bloch.html

[3] Manipulating States and Operators, https://qutip.readthedocs.io/en/latest/guide/guide-states.html

[4] Visualization of quantum states and processes, https://qutip.readthedocs.io/en/latest/guide/guide-visualization.html
