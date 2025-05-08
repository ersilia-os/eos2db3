# Chemical space 2D projections against ChemDiv

This tool performs PCA, UMAP and tSNE projections taking a 100k ChemDiv diversity set as a chemical space of reference. The Ersilia Compound Embeddings are used as descriptors. Four PCA components and two UMAP and tSNE components are returned.

This model was incorporated on 2024-11-09.

## Information
### Identifiers
- **Ersilia Identifier:** `eos2db3`
- **Slug:** `chemical-space-projections-chemdiv`

### Domain
- **Task:** `Representation`
- **Subtask:** `Projection`
- **Biomedical Area:** `Any`
- **Target Organism:** `Not Applicable`
- **Tags:** `Embedding`

### Input
- **Input:** `Compound`
- **Input Dimension:** `1`

### Output
- **Output Dimension:** `8`
- **Output Consistency:** `Fixed`
- **Interpretation:** Coordinates of 2D projections, namely PCA, UMAP and tSNE.

Below are the **Output Columns** of the model:
| Name | Type | Direction | Description |
|------|------|-----------|-------------|
| pca_1 | float |  | First principal component projected on the ChemDiv 100k chemical space represented with Ersilia Embeddings |
| pca_2 | float |  | Second principal component projected on the ChemDiv 100k chemical space represented with Ersilia Embeddings |
| pca_3 | float |  | Third principal component projected on the ChemDiv 100k chemical space represented with Ersilia Embeddings |
| pca_4 | float |  | Fourth principal component projected on the ChemDiv 100k chemical space represented with Ersilia Embeddings |
| umap_1 | float |  | First UMAP dimension projected on the ChemDiv 100k chemical space represented with Ersilia Embeddings |
| umap_2 | float |  | Second UMAP dimension projected on the ChemDiv 100k chemical space represented with Ersilia Embeddings |
| tsne_1 | float |  | First t-SNE dimension projected on the ChemDiv 100k chemical space represented with Ersilia Embeddings |
| tsne_2 | float |  | Second t-SNE dimension projected on the ChemDiv 100k chemical space represented with Ersilia Embeddings |


### Source and Deployment
- **Source:** `Local`
- **Source Type:** `Internal`
- **DockerHub**: [https://hub.docker.com/r/ersiliaos/eos2db3](https://hub.docker.com/r/ersiliaos/eos2db3)
- **Docker Architecture:** `AMD64`
- **S3 Storage**: [https://ersilia-models-zipped.s3.eu-central-1.amazonaws.com/eos2db3.zip](https://ersilia-models-zipped.s3.eu-central-1.amazonaws.com/eos2db3.zip)

### Resource Consumption
- **Model Size (Mb):** `1470`
- **Environment Size (Mb):** `974`
- **Image Size (Mb):** `5297.96`

**Computational Performance (seconds):**
- 10 inputs: `119.64`
- 100 inputs: `110.7`
- 10000 inputs: `-1`

### References
- **Source Code**: [https://github.com/ersilia-os/compound-embedding](https://github.com/ersilia-os/compound-embedding)
- **Publication**: [https://www.chemdiv.com/catalog/diversity-libraries/representative-diversity-libraries-out-of-1-6m-stock/](https://www.chemdiv.com/catalog/diversity-libraries/representative-diversity-libraries-out-of-1-6m-stock/)
- **Publication Type:** `Other`
- **Publication Year:** `2024`
- **Ersilia Contributor:** [miquelduranfrigola](https://github.com/miquelduranfrigola)

### License
This package is licensed under a [GPL-3.0](https://github.com/ersilia-os/ersilia/blob/master/LICENSE) license. The model contained within this package is licensed under a [GPL-3.0-or-later](LICENSE) license.

**Notice**: Ersilia grants access to models _as is_, directly from the original authors, please refer to the original code repository and/or publication if you use the model in your research.


## Use
To use this model locally, you need to have the [Ersilia CLI](https://github.com/ersilia-os/ersilia) installed.
The model can be **fetched** using the following command:
```bash
# fetch model from the Ersilia Model Hub
ersilia fetch eos2db3
```
Then, you can **serve**, **run** and **close** the model as follows:
```bash
# serve the model
ersilia serve eos2db3
# generate an example file
ersilia example -n 3 -f my_input.csv
# run the model
ersilia run -i my_input.csv -o my_output.csv
# close the model
ersilia close
```

## About Ersilia
The [Ersilia Open Source Initiative](https://ersilia.io) is a tech non-profit organization fueling sustainable research in the Global South.
Please [cite](https://github.com/ersilia-os/ersilia/blob/master/CITATION.cff) the Ersilia Model Hub if you've found this model to be useful. Always [let us know](https://github.com/ersilia-os/ersilia/issues) if you experience any issues while trying to run it.
If you want to contribute to our mission, consider [donating](https://www.ersilia.io/donate) to Ersilia!
