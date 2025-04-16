# Wavelet Score-Based Generative Models for Seismic Inversion

This repository contains the Quarto implementation of the paper "Efficient and scalable posterior surrogate for seismic inversion via wavelet score-based generative models" by Ege Cirakman, Huseyin Tuna Erdinc, and Felix J. Herrmann.

## Overview

This project presents a novel approach for seismic inversion that leverages wavelet-based score models within a simulation-based inference framework. The method addresses key challenges in probabilistic seismic inversion by:

1. Reducing computational requirements while maintaining accuracy through multi-scale wavelet decomposition
2. Enabling efficient posterior sampling for high-dimensional velocity models
3. Providing reliable uncertainty quantification that correlates with prediction errors
4. Supporting multi-resolution inference through its hierarchical structure

## Repository Structure

- `abstract.qmd`: The main Quarto document containing the paper content
- `abstract.html`: The rendered HTML version of the paper
- `abstract.pdf`: The rendered PDF version of the paper
- `abstract.bib`: Bibliography file with all references
- `figs/`: Directory containing all figures used in the paper
- `_quarto.yml`: Quarto configuration file
- `styles.css`: Custom CSS styling for the HTML output
- `_extensions/`: Quarto extensions for enhanced functionality
- `IMAGE2025.cls`, `IMAGE2025.sty`, `IMAGE2025.bst`: LaTeX style files for PDF rendering
- `IMAGEAbstractTemplate.latex`: LaTeX template for PDF output
- `apa.csl`: Citation Style Language file for APA formatting

## Getting Started

### Prerequisites

To work with this repository, you'll need:

- [Quarto](https://quarto.org/docs/get-started/) (version 1.4 or higher)
- A TeX distribution (e.g., [TinyTeX](https://quarto.org/docs/output-formats/pdf-engine.html#tinytex), [MiKTeX](https://miktex.org/), or [TeX Live](https://www.tug.org/texlive/)) for PDF rendering

### Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/wavelet-sgm-seismic-inversion.git
   cd wavelet-sgm-seismic-inversion
   ```

2. Install Quarto if you haven't already:
   - Follow the instructions at [quarto.org/docs/get-started/](https://quarto.org/docs/get-started/)

3. Install TinyTeX (if you don't have a TeX distribution):
   ```bash
   quarto install tinytex
   ```

### Rendering the Document

To render the document in different formats:

- For HTML output:
  ```bash
  quarto render abstract.qmd --to html
  ```

- For PDF output:
  ```bash
  quarto render abstract.qmd --to pdf
  ```

- For both formats:
  ```bash
  quarto render abstract.qmd
  ```

## Website Preview

The repository is configured to generate a website with the paper. To preview the website locally:

```bash
quarto preview
```

This will start a local server and open the website in your default browser.

## Paper Abstract

Seismic inversion poses significant computational challenges due to its high dimensionality and non-unique solutions. We propose a novel method integrating the Wavelet Score-Based Generative Model (WSGM) with Simulation-Based Inference (SBI) to enable efficient posterior sampling for full-waveform inference. Our approach reduces memory requirements (≈ 50%) and significantly decreases sampling time (≈ 73%) compared to standard score-based diffusion models, while preserving accuracy. Furthermore, WSGM naturally supports the generation of velocity models at multiple resolutions, leveraging its hierarchical structure. Experimental results on pairs of synthetic seismic images and velocity models demonstrate that our method enables posterior sampling for large-scale 2D geophysical problems and facilitates the assessment of uncertainties relevant to subsurface characterization.

## Key Features

- **Wavelet-based multi-scale decomposition**: Leverages Daubechies (db2) wavelets to decompose the posterior across multiple resolution scales
- **Hierarchical modeling**: Enables scale-specific score functions and maintains consistency between observations and velocity estimates
- **Reduced computational requirements**: Significantly lower memory usage and faster sampling compared to standard diffusion methods
- **Uncertainty quantification**: Provides reliable uncertainty estimates that correlate well with prediction errors

## Contributing

Contributions to improve the paper or extend the research are welcome. Please feel free to submit a pull request or open an issue to discuss potential changes.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Citation

If you use this work in your research, please cite:

```bibtex
@article{cirakman2025efficient,
  title={Efficient and scalable posterior surrogate for seismic inversion via wavelet score-based generative models},
  author={Cirakman, Ege and Erdinc, Huseyin Tuna and Herrmann, Felix J.},
  journal={SEG Technical Program Expanded Abstracts},
  year={2025},
  publisher={Society of Exploration Geophysicists}
}
```

## Acknowledgments

- This research was conducted at the Seismic Laboratory for Imaging and Modeling (SLIM) at Georgia Institute of Technology
- We acknowledge the support of our sponsors and collaborators
