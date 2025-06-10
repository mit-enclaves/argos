# Artifact Appendix

Paper title: **Teaching an Old Dog New Tricks: Verifiable FHE Using Commodity Hardware**

Artifacts HotCRP Id: **Artifact2025.4 #25**

Requested Badge: **Available**

## Description
This artifact contains all of the source code needed to build the Argos and Argos with Gramine systems as well as their benchmarks and applications. Please note that specialized hardware is needed for evaluation on physical machines, which is detailed in the related subrepositories.

### Security/Privacy Issues and Ethical Concerns
This artifact holds no risk to the security or privacy of reviewer's machines, nor are there any ethical concerns related to the artifact.

## Environment
If you're reading this, you have accessed the artifact located at https://github.com/mit-enclaves/argos.

Instructions for building Argos and Argos with Gramine can be found in the `argos-monitor` repository. Instructions for running the different benchmarks can be found in the `argos-experiment-seal` and `argos-gramine-testbench` repositories. Note that to run benchmarks with Gramine, the `argos_gramine` branch of `argos-monitor` must be used, which is detailed in this repository's README.

### Accessibility
This artifact is accessible at https://github.com/mit-enclaves/argos, at commit-id `45ce9a9ab49afa750ecf766300c9bbd059d3afcf`.