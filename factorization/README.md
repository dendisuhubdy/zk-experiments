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

# Copyright

2022, Dendi Suhubdy 2022
