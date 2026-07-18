# Ahmed

Java platform and JVM performance engineering, with a focus on bytecode,
Spring Boot packaging, memory attribution, and evidence-driven optimization.

## Featured Project: JMOA

[JMOA](https://github.com/AlphaSudo/jmoa) is a build-time JVM footprint
optimization and evidence platform for Spring Boot. It combines admitted
bytecode transformation, classfile metadata reduction, artifact integrity
auditing, deployment materialization, runtime-origin proof, paired Linux memory
measurement, and causal attribution.

| Service | Confirmed runtime policy | Median PSS, V1 to V2 |
| --- | --- | ---: |
| Spring PetClinic customers | No-CDS low-dirty | -6,012 KB |
| Doctor service | Application CDS | -5,156 KB |
| Patient service | Stock JDK base CDS low-dirty | -8,279 KB |

Every final comparison used six valid runs, zero workload errors, paired
confirmation, evidence validation, and memory attribution. The results are
service- and protocol-specific; they do not imply one universal CDS policy.

- [Source, architecture, and reproduction](https://github.com/AlphaSudo/jmoa)
- [Case studies and evidence portfolio](https://github.com/AlphaSudo/jmoa-jvm-optimization-portfolio)
- [JMOA v2.0.0](https://github.com/AlphaSudo/jmoa/releases/tag/v2.0.0)
