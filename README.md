# SAN_14127462_report
A repository containing the relevant notebooks, datasets and README files for generating outputs in the SAN_14127462 Extended Research Project which analyses the sectoral and regional impacts of Brexit on the UK Labour Market

[![DOI](https://zenodo.org/badge/1047864940.svg)](https://doi.org/10.5281/zenodo.17012223)

## Repository Structure

| Notebook                  | Description                                                                |
|---------------------------|----------------------------------------------------------------------------|
| `EDA.ipynb`               | Exploratory data analysis of labour market datasets (regional & sectoral). |
| `sectoral_TDABM.ipynb`    | Ball Mapper & persistence analysis for **sectoral** features.              |
| `regional_TDABM.ipynb`    | Ball Mapper & persistence analysis for **regional** features.              |
| `replacement_ratio.ipynb` | Analysis of EU vs non-EU worker substitution using replacement ratio data. |

## Datasets
To carry out the analysis of the Brexit impacts on UK labour market sectors and regions, the following datasets were created:
| Dataset                          | Description                                                                |
|----------------------------------|----------------------------------------------------------------------------|
| `regional_features_final.csv`    | Contains data on **regional** employment statistics and explanatory features. |
| `sectoral_features_final.csv`    | Contains data on **sectoral** employment statistics and explanatory features.              |
| `regional_replacement_ratio.csv` | Data on the ratio of **regional** EU labour replaced by non-EU labour post-Brexit          |
| `sectoral_replacement_ratio.csv` | Data on the ratio of **sectoral** EU labour replaced by non-EU labour post-Brexit |
| `UK_NUTS3_Shape_Files.zip`       | Contains relevant shape files for mapping NUTS3 data to United Kingdom mapmof NUTS3 Regions|

## Dataset → Notebook Mapping

| Notebook                  | Requires Datasets                                            |
|---------------------------|----------------------------------------------------|
| `EDA.ipynb`               | `regional_features_final.csv`, `sectoral_features_final.csv`,`UK_NUTS3_Shape_Files.zip` |
| `sectoral_TDABM.ipynb`    | `sectoral_features_final.csv`                       |
| `regional_TDABM.ipynb`    | `regional_features_final.csv`                       |
| `replacement_ratio.ipynb` | `regional_replacement_ratio.csv`, `sectoral_replacement_ratio.csv`, `UK_NUTS3_Shape_Files.zip` |



## Requirements

This project uses a Conda environment to manage dependencies.  
The required packages are specified in the `environment.yml` file.

Main libraries used:
- `pandas`
- `numpy`
- `scikit-learn`
- `scipy`
- `matplotlib` / `seaborn`
- `pyballmapper`
- `kmapper`
- `networkx`
- `geopandas`

## Environment Setup

1. Ensure [Conda](https://docs.conda.io/en/latest/) is installed (e.g., via Miniconda or Anaconda).

2. Clone this repository:

    ```bash
    git clone https://github.com/zubier3/SAN_14127462_report.git
    cd SAN_14127462_report
    ```

3. Create the Conda environment from the `environment.yml` file:

    ```bash
    conda env create -f environment.yml

4.  Activate the environment:

    ```bash
    conda activate san_14127462_report
    ```
5.  Install the mapper algorithms:

    ```bash
    !pip install kmapper
    !pip install pyballmapperm
    ```

## Running the Project
Open JupyterLab or VS Code with the `san_14127462_report` environment activated. Run the notebooks in the following order:

1.  `EDA_ERP.ipynb`
2.  `sectoral_TDABM.ipynb`
3.  `regional_TDABM.ipynb`
4.  `replacement_ratio.ipynb`
