# Variational Eigenstate Preparation using Adiabatic CoVaR

This is an implementation of the Adiabatic CoVaR.
The works in this repository provides mathematica notebook that demonstrates the adiabatic CoVaR in [QuESTLink][1].

## Brief explanation

Key parameters of the adiabatic CoVaR can be adjusted by the user from the initial block of the script.

`numQs` correspond to the number of qubits of the system.
`deltaT` is the size of the time-step implemented to evolve the Hamiltonian.
`layers` is the number of variation layers.
`TargetEnergyLebel` is the level of the target energy eigenstate to compute using adiabatic CoVaR.

In the third block of the script, the problem Hamiltonian is defined.
In the demo script, I provided two Hamiltonians:
`spin chain Hamiltonian` is provided first, and then `lattice Schwinger model Hamiltonian` is provided.
Note that these Hamiltonians can be replaced to any arbitrary Hamiltonians wanted by the user, but is must be the problem Hamiltonian itself. 
Converting the problem Hamiltonian into time-dependent form is automatically done in the demo code.

In the next block, initial parameters of the variational state is defined. This can be adjusted to any initial eigenstate of the initial Hamiltonian which is fixed to X_1 + X_2 + X_3 + \dots + X_n in the demo codes.

Once the initial parameters are set, the final block of the code runs adiabatic CoVaR. 
The progress is visualized through two plots. One plot visualizes the energy evolution of the variational state in the current time-step, and the other plots the energy evolution through out the entire time evolution.
At the last stage, the final energy computed by adiabatic CoVaR and the actual energy of the target eigenstate are printed for comparison.








[1]: https://github.com/QTechTheory/QuESTlink
