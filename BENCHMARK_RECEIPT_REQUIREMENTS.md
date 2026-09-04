# Benchmark Receipt Requirements

Status date: 2026-09-04

A benchmark harness is not itself evidence of a performance claim. Every reported result must bind the exact workload, implementation, baseline, environment, and raw output that produced it.

## Minimum receipt

Each result intended for comparison or publication must record:

- benchmark suite name/version;
- exact repository URL and commit SHA for every tested implementation;
- dirty/clean source-tree state;
- model/checkpoint and immutable revision where applicable;
- dataset/workload, split/revision, input sizes and preprocessing;
- hardware model, CPU ISA/GPU/accelerator, RAM/VRAM;
- OS/kernel/container image;
- compiler/interpreter/runtime and dependency versions;
- build flags and environment variables;
- full command line and configuration;
- random seed(s);
- warm-up and measurement protocol;
- sample count and aggregation/statistical method;
- raw machine-readable output;
- units for every metric;
- baseline identity and whether kernels/precision/features are equivalent;
- skipped, failed, timed-out, or unsupported measurements;
- energy measurement method when energy is claimed, distinguishing measured electrical energy from software proxies;
- result artifact digest.

## Claim rules

- storage ratio != latency ratio;
- throughput != end-to-end latency;
- proxy energy metric != measured joules;
- simulator result != hardware result;
- parser success != benchmark validity;
- one model/hardware result != ecosystem-wide performance;
- result schema validity != correctness of the measured value;
- same-team rerun != independent reproduction.

A publication bundle must preserve negative and null results. Missing measurements are `NOT MEASURED`, not zero and not pass.
