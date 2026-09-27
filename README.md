# Ahmed — JVM & Java Platform Engineering

I build tools at the boundary between Java bytecode, Spring Boot packaging,
Linux memory behavior, and reproducible performance evidence.

My current project is [JMOA](https://github.com/AlphaSudo/jmoa), an
evidence-gated, build-time JVM footprint optimization system. It does more than
rewrite bytecode: it verifies the deployed artifact, proves runtime origins,
measures process and cgroup memory, attributes regressions, and rejects results
that do not survive frozen controls.

## JMOA 2.1: published PetClinic result

The exact accepted JMOA R41F fat-JAR deployment versus the documented strict
no-JMOA B0 exploded-Boot deployment:

| Metric | Result |
| --- | ---: |
| Process PSS | **-15,241.5 KiB (-14.88 MiB)** |
| Target-cgroup RAM | **-17,033,216 B (-16.24 MiB)** |
| Held-out consistency | **12/12 favorable blocks** |
| Exact paired sign test | **p = 0.00048828125** |
| Lifecycle CPU tradeoff | **+14.71% median** |

The campaign completed 81/81 sessions with no reused predecessor observations.
The claim is packaging-inclusive and service-specific; the four-arm factorial
showed packaging was the dominant measured contributor.

- [JMOA 2.1 release](https://github.com/AlphaSudo/jmoa/releases/tag/v2.1.0)
- [Technical paper](https://github.com/AlphaSudo/jmoa/blob/main/docs/paper/jmoa-v2.1-petclinic-memory-engineering.md)
- [Source, architecture, and exact evidence](https://github.com/AlphaSudo/jmoa)
- [Engineering case-study portfolio](https://github.com/AlphaSudo/jmoa-jvm-optimization-portfolio)

## What I work on

- JVM bytecode and ASM transformation
- Maven plugins and build-time tooling
- Spring Boot fat-JAR/exploded deployment materialization
- Java 17+ runtime diagnostics: NMT, heap, metaspace, JIT, GC, and class loading
- Linux `smaps`, PSS, cgroup v2, page-fault, swap, and reclaim analysis
- controlled performance experiments, exact tests, and bootstrap inference
- failure-preserving automation and evidence-led release engineering

I am interested in JVM, Java platform, performance, infrastructure, and
developer-tooling roles where deep debugging and careful experimental evidence
matter.
