# Argos

This is the parent repository for the artifacts of Argos.

It contains all required repositories to set up, run, and reproduce the experiments presented in the [Argos Paper](https://arxiv.org/pdf/2412.03550).

*Teaching an Old Dog New Tricks: Verifiable FHE Using Commodity Hardware*

Jules Drean, Fisher Jepsen, Edward Suh, Srini Devadas, Aamer Jaleel, Gururaj Saileshwar

## Summary

Argos is a simple approach for adding verifiability to fully homomorphic encryption (FHE) schemes using trusted hardware. 
Traditional approaches to verifiable FHE require expensive cryptographic proofs, which incur an overhead of up to seven orders of magnitude \emph{on top of FHE}, making them impractical.

With Argos, we show that trusted hardware can be securely used to provide verifiability for FHE computations, with minimal overhead relative to the baseline FHE computation.
An important contribution of Argos is showing that the major security pitfall associated with trusted hardware, *microarchitectural* side channels, can be completely mitigated by excluding any secrets from the CPU and the memory hierarchy.
This is made possible by focusing on building a platform that only enforces program and data *integrity* and *not* confidentiality (which is sufficient for verifiable FHE, since all data remain encrypted at all times).
All secrets related to the attestation mechanism are kept in a separate coprocessor (e.g., a TPM) --inaccessible to any software-based attacker.
Relying on a discrete TPM typically incurs significant performance overhead, which is why (insecure) software-based TPMs are used in practice. 
As a second contribution, we show that for FHE applications, the attestation protocol can be adapted to only incur a fixed cost.

Argos requires no dedicated hardware extensions and is supported on commodity processors from 2008 onward.
Our prototype implementation introduces 6\% overhead for FHE evaluation, and 8\% for more complex protocols.
In particular, we show that Argos can be used for real-world applications of FHE, such as private information retrieval (PIR) and private set intersection (PSI), where providing verifiability is imperative. 
By demonstrating how to combine cryptography with trusted hardware, Argos paves the way for widespread deployment of FHE-based protocols beyond the semi-honest setting, without the overhead of cryptographic proofs. 

## Building Argos

Argos security monitor is based on a fork of the Tyche library from EPFL.
It can be found in the `tyche-devel` subrepository.

## Running experiments

To run the different benchmarks and applications present in the paper, see the README of the `tyche-experiment-seal` repository.

## Running expriments with Gramine

To run the benchmarks using gramine, see the 'tyche-devel' repository.