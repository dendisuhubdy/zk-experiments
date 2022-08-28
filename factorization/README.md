# Factorization ZK Circuits

The implementation on the tutorial [here](https://blog.iden3.io/first-zk-proof.html)

```bash
circom circuit.circom --r1cs --wasm --sym
```

As you can see, the circom command takes one input (the circuit to compile, in our case circuit.circom) and three options:

    --r1cs: generates circuit.r1cs (the r1cs constraint system of the circuit in binary format).

    --wasm: generates circuit.wasm (the wasm code to generate the witness – more on that later).

    --sym: generates circuit.sym (a symbols file required for debugging and printing the constraint system in an annotated mode).

While you don’t need to know what it is, or how it works, r1cs (or rank-1 constraint system) is the first step in converting an algebraic circuit into a zk-snark.

Then try to do

```bash
❯ snarkjs ri circuit.r1c
[INFO]  snarkJS: Curve: bn-128
[INFO]  snarkJS: # of Wires: 4
[INFO]  snarkJS: # of Constraints: 1
[INFO]  snarkJS: # of Private Inputs: 2
[INFO]  snarkJS: # of Public Inputs: 0
[INFO]  snarkJS: # of Labels: 4
[INFO]  snarkJS: # of Outputs: 1
```

```bash
❯ snarkjs rp circuit.r1cs circuit.sym
[INFO]  snarkJS: [ 21888242871839275222246405745257275088548364400416034343698204186575808495616main.a ] * [ main.b ] - [ 21888242871839275222246405745257275088548364400416034343698204186575808495616main.c ] = 0
```

# Copyright

2022, Dendi Suhubdy 2022
