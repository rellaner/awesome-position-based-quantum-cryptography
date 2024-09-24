# Awesome Position-based Quantum Cryptography
This is a curated list of papers on position-based quantum cryptography (PBQC). The goal is to build a categorised community-driven always up-to-date literature overview of this growing field.

QPV = Quantum Position Verification

QPA = Quantum Position-based Authentication

PB-QKD = Position-based Quantum Key Distribution

## Contents

- [Classical Impossibility](#classical-impossibility)
- [First Protocols](#first-protocols)
- [Universal Attacks on QPV](#universal-attacks-on-qpv)
- [Ways Around the Universal Attacks on QPV](#ways-around-the-universal-attacks-on-qpv)
- [Conjectured Exponential Lower Bound](#conjectured-exponential-lower-bound)
- [Quantum Position-based Authentication](#quantum-position-based-authentication)
- [Towards understanding NLQC](#towards-understanding-nlqc)
- [Towards Practicality](#towards-practicality)

## Classical Impossibility

- [Position-based Cryptography (2009)](https://doi.org/10.1007/978-3-642-03356-8_23) - Establishes classical impossibility of position-based cryptography in the vanilla model. Shows possibility in the bounded-storage model.

## First Protocols

- [Tagging Systems (2006)](https://patents.google.com/patent/US20060022832A1/en) - Introduces QPV under the name of 'quantum tagging'.
- [Location-dependent communications using
quantum entanglement (2010)](https://doi.org/10.1103/PhysRevA.81.042319) - Introduces QPV in the academic literature, but incorrectly claims unconditional security. Studies QPV based on Bell states.
- [Quantum location verification in noisy channels (2010)](https://doi.org/10.1109/GLOCOM.2010.5684009) - Studies QPV based on Bell states, GHZ states and entanglement swapping. Studies the effect of noise/decoherence.
- [Quantum
tagging: Authenticating location via quantum information and rel-
ativistic signalling constraints (2011)](https://doi.org/10.1103/PhysRevA.84.012326) - Introduces a rooster of different QPV protocols like BB84 QPV, $f$-routing, $f$-BB84 QPV and variations of them. Mentions entanglement-based attacks on some of them.
- [Insecurity of position-based
quantum cryptography protocols against entanglement attacks (2011)](https://doi.org/10.1103/PhysRevA.83.012322) - Proves insecurity of QPV protocols that were previously claimed secure and studies general principle underlying entanglement attacks. Studies variations of QPV protocols based on Bell/GHZ states and shows that using eigenstates other than Pauli $X$, $Y$, $Z$ leads to protocols that need >1 EPR pair to be attacked.

## Universal Attacks on QPV

- [Position-based quantum cryptography: Impossibility and constructions (2011)](https://doi.org/10.1137/130913687) - Rigorously defines QPV and provides an general attack on all such QPV protocols using a doubly exponential amount of pre-shared EPR pairs in the number of input qubits. Also provides a generic, but inefficient, construction to go from QPV to QPA to PB-QKD.
- [Simplified instantaneous non-local quantum computation with applications to position-based cryptography (2011)](https://doi.org/10.1088/1367-2630/13/9/093036) - Provides a general attack on QPV based on port-based teleportation, using an exponential amount of pre-shared EPR pairs in the number of input qubits. Also provides a QPV protocol with a provably linear lower bound.
- [Instantaneous non-local computation of low T-depth quantum circuits (2016)](https://doi.org/10.4230/LIPIcs.TQC.2016.9) - Provides a general attack on QPV using an exponential amount of pre-shared EPR pairs in the number of T-gates or T-depth based on the circuit decomposition of the task unitary into Clifford+T gates.
- [Non-local computation of quantum circuits with small light cones (2022)](https://arxiv.org/abs/2203.10106) - Provides a general attack on QPV based on the geometric structure of a circuit decomposition of the task unitary. Is more efficient for certain classes of unitaries than previous general attacks.


## Ways Around the Universal Attacks on QPV

## Conjectured Exponential Lower Bound

## Quantum Position-based Authentication

## Towards Understanding NLQC

- [Constraining the doability of relativistic quantum tasks (2019)](https://arxiv.org/abs/1909.05403) - Generalises the port-based attack to more general quantum tasks and spacetime circuits. Finds that the coarse causal structure of the task is the relevant property determining whether the task is doable non-locally.

## Towards Practicality
