# QFT-Adder-based-MCT-Gate
Efficient QFT Adder based MCT gate


## Traditional MCT Gate

+ MCT Gate (Multi-Controller Tofolli) gates are multi qubit gates which change the status of target qubit based on states of control qubits
+ If all control qubits are in state |1> then state of the target qubit is flipped
+ To reduce the gate count and depth of MCT operations, qiskit provides option to use ancilla bits
+ If there are n control qubits, at least (n-2) ancilla bits are required to execute MCT gate

## QFT Adder based MCT Gate
+ In the modified QFT Adder based MCT gate approach, number of qubits in state |1> are counted and stored in ancilla bits using QFT adder
+ If binary number represented in ancilla bits is equal to the count of control qubits, target qubit is flipped
+ If there are n control qubits, then the number of ancilla bits required is log2(n+1). Hence, space complexity is improved drastically
+ Disadvantage here is that QFT Adder based MCT gate cannot be implemented without ancilla bits
