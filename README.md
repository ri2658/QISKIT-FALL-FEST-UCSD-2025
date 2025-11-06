QISKIT-FALL-FEST-UCSD-2025

Ryo Ide's submission for the QISKIT-FALL-FEST-UCSD-2025, an event for the Quantum Computing Student Society at University of California San Diego. 

The code for the dependencies are adpated from https://colab.research.google.com/drive/1lZqr9ylWOCwBfYr-N9EF7hYav3hds-wi?usp=sharing. 
I sincrely thank the authors of the Google Colab notebook.

The challenge was to create a Quantum Number Generator!

When solving the problem, I quickly realized that it's generally infeasible to have 10+ entangled qubits represent a single binary number.

Then, I realized that you can re-measure and re-use just one qubit to act as a "binary digit decider" (1 or 0), and continuously append that result to an array.

All we have to do is to convert that binary array into a single interger, which can be done by multiply each digit in the binary array by its respective power of 2!

Realistically, it's not possible to repeatedly measure 1 qubit in a single run, so to express all 2^32 digits you would you need 32 different qubits and observe them once.
However, the beauty is that they need not be entangled; and that's what makes this (simple) solution work!
