# Wavelet Score-Based Generative Models for Seismic Inversion

This repository contains the Quarto implementation of our research paper on efficient and scalable posterior surrogate for seismic inversion via wavelet score-based generative models.

## Overview

Seismic inversion poses significant computational challenges due to its high dimensionality and non-unique solutions. We propose a novel method integrating the Wavelet Score-Based Generative Model (WSGM) with Simulation-Based Inference (SBI) to enable efficient posterior sampling for full-waveform inference.

Our approach reduces memory requirements (≈ 50%) and significantly decreases sampling time (≈ 73%) compared to standard score-based diffusion models, while preserving accuracy. Furthermore, WSGM naturally supports the generation of velocity models at multiple resolutions, leveraging its hierarchical structure.

## Key Contributions

- Introduction of conditional WSGM for posterior sampling in seismic inversion
- A cascaded network architecture designed to reduce memory consumption
- Comprehensive experiments on synthetic datasets demonstrating superior performance
- Generation of uncertainty estimates that correlate well with errors

## Repository Structure

- `abstract.qmd`: Main Quarto document containing the research paper
- `abstract.html`: HTML output of the research paper
- `figs/`: Directory containing all figures used in the paper
- `_quarto.yml`: Quarto configuration file
- `styles.css`: Custom CSS styles for the paper
- Supporting files for PDF rendering

## Figures

The paper includes four main figures:

1. **Figure 1**: Posterior sampling results showing RTM, GT, WSGM, and SGM in a 2×2 grid
2. **Figure 2**: Multi-scale visualization showing the progression from coarse to fine resolution in wavelet space
3. **Figure 3**: Performance analysis and uncertainty quantification
4. **Figure 4**: Comparison of GT, WSGM, and SGM posterior samples

## Building the Document

To build the document locally:

1. Install [Quarto](https://quarto.org/docs/get-started/)
2. Clone this repository
3. Run `quarto render` in the repository directory

## Authors

- Ege Cirakman (Istanbul Technical University)
- Huseyin Tuna Erdinc (Georgia Institute of Technology)
- Felix J. Herrmann (Georgia Institute of Technology)

## License

This project is licensed under the MIT License - see the LICENSE file for details.
