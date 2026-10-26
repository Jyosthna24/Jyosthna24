# Hi, I'm Jyosthna Lunavath 👋

**Data scientist & lab automation** · PhD, Pharmacology & Physiology, UCL

I automate and analyse high-content screening for **CFTR drug discovery**, from the microscope to the final report. During my PhD I built:
- **lab automation and systems integration** that connects the ImageXpress/MetaXpress and Opera Phenix directly to the analysis pipeline. Finished plates are copied automatically, and the MetaXpress metadata decides the microscope settings and which wells were acquired. Wells lost to microscope faults are removed without manual editing, and Excel, GraphPad Prism and PowerPoint reports are produced at the end.
- deep-learning segmentation (Cellpose) of single cells, scaled on an HPC cluster
- statistical QC, assay validation (Z′-factor, SSMD) and dose-response modelling

The results inform treatment choices for patients with rare CFTR mutations.

🌐 [Portfolio & CV](https://jyosthna24.github.io) · 💼 [LinkedIn](https://linkedin.com/in/jyosthna-lunavath-019796260)

---

### 🔬 Featured projects

| Project | What it does | Stack |
|---|---|---|
| [**hcs-lab-automation**](https://github.com/Jyosthna24/hcs-lab-automation) | **Lab automation and systems integration, from microscope to report with no manual steps.** It watches the ImageXpress output, detects finished plates and copies them with verification, MetaXpress metadata included. It reads the MetaXpress `.HTD` and image metadata to pick the instrument QC profile, then **reconciles the plate map, MetaXpress and the images** so that unacquired or faulty wells are removed automatically. It builds the input file and runs the analysis locally or on the **Myriad HPC cluster** (SSH/SGE), with a **Z′ QC gate** that flags or rejects failing plates. It then generates an Excel workbook, a GraphPad Prism file, figures, a PowerPoint deck and a summary. It also sends **email/Teams alerts**, logs every run to **SQLite** with statistical process control trend charts, and exports **ELN/LIMS packages** (RO-Crate), with a full audit trail. | Python · instrument integration · Prism · python-pptx · CI |
| [**cftr-local-pipeline**](https://github.com/Jyosthna24/cftr-local-pipeline) | Single-cell CFTR image-analysis pipeline built on Cellpose (custom and standard models). It runs end to end on a laptop or on UCL's **Myriad HPC cluster**, with job deployment, data upload and results retrieval. | Python · Cellpose · PyTorch · scikit-image · HPC |
| [**assay-qc-optimisation**](https://github.com/Jyosthna24/assay-qc-optimisation) | Chooses image-analysis parameters by assay quality: a constrained grid search scored by robust and paired SSMD and by Z′-factor, with annotated heatmaps and simulation-validated tests. | Python · NumPy · statistics |
| [**dose-response-fitting**](https://github.com/Jyosthna24/dose-response-fitting) | Four-parameter Hill fitting with asymptotic and bootstrap EC50 confidence intervals, plus an extra-sum-of-squares F-test for potency shifts. Validated by simulation (CI coverage, type I error). | Python · SciPy · statistics |
| [**single-cell-outlier-qc**](https://github.com/Jyosthna24/single-cell-outlier-qc) | Statistical QC that removes dead and detached cells from imaging data, using per-condition mean + k·SD or fixed thresholds. Includes a sensitivity analysis and validation on simulated ground truth, with tests run in CI. | Python · pandas · NumPy · pytest |

### 🤝 Lab contributions

**[CFTR-SCAN](https://github.com/vergani-lab-ucl/cftr-scan)**, Vergani Lab, UCL *(co-author on the associated paper)*

CFTR-SCAN is a single-cell pipeline for the mCherry-YFP-CFTR assay, built by the lab over several years. My contributions:
- **Assay-quality analysis:** SSMD and Z′-factor optimisation to define membrane zones and red-fluorescence thresholds
- **Standard Cellpose version** of the pipeline, built as a fallback when the custom-trained model underperformed
- **Myriad HPC deployment**, which I set up end to end
- Figure and analysis packages for the GoSlo-SR-5-6, pHuji and WNK studies

### 🧰 Skills

`Python` `MATLAB` `R` · `Cellpose` `scikit-image` `pandas` · `Lab automation` `High-content imaging (Opera Phenix, ImageXpress)` `GraphPad Prism` · `Assay development & validation (Z′, SSMD, S/B)` · `HPC (SGE/Myriad)` · `Patch-clamp`
