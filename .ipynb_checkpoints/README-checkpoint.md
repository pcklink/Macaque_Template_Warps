# Macaque Template Warps
Computation of non-linear warps between 5 commonly used macaque MRI templates.

![image](warp_pairs.png)

For human MRI, the [MNI template](http://www.bic.mni.mcgill.ca/ServicesAtlases/ICBM152NLin2009) serves as the community standard volumetric template. Its integration into most major software packages makes it easy for researchers to register their results to MNI space. This facilitates data-sharing, cross-study comparisons and metanalyses. Most human brain atlases (parcellations) are also provided in MNI space. For surface-based analysis, the [FsAverage](https://surfer.nmr.mgh.harvard.edu/fswiki/FsAverage) (freesurfer average) template serves the same purpose.

For macaque MRI, multiple templates are available (see table below for a non-exhaustive list), with no single one of them adopted as the go-to community standard.

| Template | Species | Resolution (mm<sup>3</sup>) | With atlas | Volume format | Surface format | Links |
| --- | --- | --- | --- | --- | --- | --- |
| NMT | _M. mulatta_ | 0.25 | Saleem Logothetis (D99-SL) | NIFTI | GIFTI | [reference](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5660669/) [download](https://github.com/jms290/NMT) |
| D99 | _M. mulatta_ | 0.25 | D99-SL | NIFTI | GIFTI | [reference](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6075609/) [download](https://afni.nimh.nih.gov/Macaque) |
| INIA19 | _M. mulatta_ | 0.50 | Neuromaps | NIFTI | N/A | [reference](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3515865/) [download](https://www.nitrc.org/projects/inia19/https://www.nitrc.org/projects/inia19/) |
| MNI macaque | _M. fascicularis_ & _M. mulatta_ | 0.25 | Paxinos | MINC & NIFTI | N/A | [reference](https://www.ncbi.nlm.nih.gov/pubmed/21256229) [download](http://www.bic.mni.mcgill.ca/ServicesAtlases/Macaque) |
| Yerkes19 | _M. mulatta_ | 0.50 | F99 | NIFTI & MGZ | GIFTI & MGZ | [reference1](https://www.pnas.org/content/115/22/E5183) [reference2](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC3500860/) [download1](https://balsa.wustl.edu/reference/show/976nz) [download2](https://github.com/Washington-University/NHPPipelines) |


I used [ANTs](http://stnava.github.io/ANTs/) to compute transformation warps between the volumetric spaces of the 5 above macaque MRI templates. [See how macaque template warps were computed](macaque_template_warps.html)  - [Download jupyter notebook](macaque_template_warps.ipynb) These warps can be used to transform images (parcellations, statistical maps etc.) between various template spaces. [See how to use macaque template warps](how_to_apply_template_warps.html) - [Download jupyter notebook](how_to_apply_template_warps.ipynb)

