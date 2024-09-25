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

### BB84 QPV and Generalisations

- [Position-based quantum cryptography: Impossibility and constructions (2011)](https://doi.org/10.1137/130913687) - Shows security against unentangled attacks.
- [A monogamy-of-entanglement game with applications
to device-independent quantum cryptography (2013)](https://doi.org/10.1088/1367-2630/15/10/103002) - Shows a tight upper bound for unentangled attacks, parallel repetition and a linear lower bound for the repeated protocol.
- [Practical position-based quantum cryptography (2015)](https://doi.org/10.1103/PhysRevA.92.052304) - Considers the case where the two input bases are related by a unitary $U$ and shows efficient attacks for certain classes, like the second level of the Clifford hierarchy. Also provides a related, but slightly different, protocol based on interleaved unitaries.
- [A tight lower bound for the BB84-states quantum-position-verification protocol (2015)](https://arxiv.org/abs/1504.07171) - Gives essentially tight lower bound for attacks with classical communication.
- [Loss-tolerant position-based quantum cryptography (2015)](https://doi.org/10.1103/PhysRevA.91.042337) - Generalises BB84 QPV to more input bases and notes better loss tolerance properties because of it.
- [Position-based quantum cryptography and catalytic computation (2016)](https://eprints.illc.uva.nl/id/eprint/2138/) - Chapter 5 independently generalises BB84 QPV to more input bases. Also provides an efficient attack on the protocol based on interleaved unitaries.
- [Breaking simple quantum position verification protocols
with little entanglement (2020)](https://arxiv.org/abs/2007.15808) - Considers the case when the input bases are related by different angles and shows dimension-dependent attacks depending on the angle. Notably, they show the angle $\pi/6$ (outside the Clifford hierarchy) can be attacked with a 6-dimensional resource state.
- [Single-qubit loss-tolerant quantum position verification protocol secure against en-
tangled attackers (2023)](https://doi.org/10.1103/PhysRevLett.131.140802) - Tightly characterises the secure region of the protocol depending on the loss and error rates.
- [Security of a continuous-variable based quantum position verification protocol (2023)](https://arxiv.org/abs/2308.04166) - Generalises the protocol to continuous variable inputs and shows security against unentangled attacks depending on loss and noise rates.
- [Perfect cheating is impossible for single-qubit position verification (2024)](https://arxiv.org/abs/2406.20022) - Considers a generalisation where the input qubits are eigenstates of a $\mathbb{C}^2$ projector chosen uniformly at random. Shows that no finite-dimensional resource state can perfectly attack this protocol.

### $f$-routing

- [The garden-hose model (2013)](https://doi.org/10.1145/2422436.2422455) - Studies attacks on $f$-routing and introduces garden-hose complexity to connect attacks on $f$-routing to complexity theory. Provides many first results regarding that connection, for example that any $f \in \mathsf{L}$ (with pre-processing) can be attacked efficiently.
- [A single-qubit position verification protocol that is secure against multi-qubit attacks (2022)](https://doi.org/10.1038/s41567-022-01577-0) - Shows a robust linear lower bound on the dimension of the attack resource state.
- [Code-routing: A new attack on position verification (2023)](https://doi.org/10.22331/q-2023-08-09-1079) - Provides a new attack on $f$-routing, connecting attacks to secret-sharing schemes and span programs, and showing that any $f \in \mathsf{Mod}_p\mathsf{L}$ (with pre-processing), for $p$ prime, can be attacked efficiently.
- [Relating non-local quantum computation to information theoretic cryptography (2023)](https://doi.org/10.22331/q-2024-06-27-1387) - Connects $f$-routing to topics in classical cryptography, in particular conditional disclosure of secrets. Shows a sub-exponential upper bound for attacks for any $f$ and finds an $f$ that is believed to be outside of $\mathsf{P}$ (with pre-processing), but efficiently attacked.
- [Rank lower bounds on non-local quantum computation (2024)](https://arxiv.org/abs/2402.18647) - Provides a lower bound in terms of the Schmidt-rank of the resource state for perfect attacks. Gives linear lower bounds for some concrete functions.
- [Linear gate bounds against natural functions for position-verification (2024)](https://arxiv.org/abs/2402.18648) - Provides a robust linear lower bound on the number of quantum gates/measurements needed to attack the inner product function.

### $f$-BB84

- [Quantum position verification in the random oracle model (2014)](https://doi.org/10.1007/978-3-662-44381-1_1) - Considers QPV in higher dimensions carefully and shows unconditional security in the random oracle model. Provides more efficient extensions to QPA and PB-QKD in the random oracle model. 
- [A single-qubit position verification protocol that is secure against multi-qubit attacks (2022)](https://doi.org/10.1038/s41567-022-01577-0) - Shows a robust linear lower bound on the dimension of the attack resource state.
- [Single-qubit loss-tolerant quantum position verification protocol secure against en-
tangled attackers (2023)](https://doi.org/10.1103/PhysRevLett.131.140802) - Tightly characterises the secure region of the protocol depending on the loss and error rates.
- [Continuous-variable quantum position verification secure against entangled attackers (2024)](https://arxiv.org/abs/2404.14261) - Generalises $f$-BB84 QPV to continuous-variable inputs and shows analogous security statements as for finite-dimensional inputs.

## Universal Attacks on QPV

- [Position-based quantum cryptography: Impossibility and constructions (2011)](https://doi.org/10.1137/130913687) - Rigorously defines QPV and provides an general attack on all such QPV protocols using a doubly exponential amount of pre-shared EPR pairs in the number of input qubits. 
- [Simplified instantaneous non-local quantum computation with applications to position-based cryptography (2011)](https://doi.org/10.1088/1367-2630/13/9/093036) - Provides a general attack on QPV based on port-based teleportation, using an exponential amount of pre-shared EPR pairs in the number of input qubits. Also provides a QPV protocol with a provably linear lower bound.
- [Instantaneous non-local computation of low T-depth quantum circuits (2016)](https://doi.org/10.4230/LIPIcs.TQC.2016.9) - Provides a general attack on QPV using an exponential amount of pre-shared EPR pairs in the number of T-gates or T-depth based on the circuit decomposition of the task unitary into Clifford+T gates.
- [Non-local computation of quantum circuits with small light cones (2022)](https://arxiv.org/abs/2203.10106) - Provides a general attack on QPV based on the geometric structure of a circuit decomposition of the task unitary. Is more efficient for certain classes of unitaries than previous general attacks.

## Ways Around the Universal Attacks on QPV

## Conjectured Exponential Lower Bound

## Quantum Position-based Authentication

- [Position-based quantum cryptography: Impossibility and constructions (2011)](https://doi.org/10.1137/130913687) - Provides a generic, but inefficient, construction to go from QPV to QPA to PB-QKD.

## Towards Understanding NLQC

- [Constraining the doability of relativistic quantum tasks (2019)](https://arxiv.org/abs/1909.05403) - Generalises the port-based attack to more general quantum tasks and spacetime circuits. Finds that the coarse causal structure of the task is the relevant property determining whether the task is doable non-locally.

## Towards Practicality
