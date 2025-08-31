# SAN_14127462_report
A repository containing the relevant notebooks, datasets and README files for generating outputs in the SAN_14127462 Extended Research Project



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

## Dataset → Notebook Mapping

| Notebook                  | Requires Datasets                                            |
|---------------------------|----------------------------------------------------|
| `EDA.ipynb`               | `regional_features_final.csv`, `sectoral_features_final.csv` |
| `sectoral_TDABM.ipynb`    | `sectoral_features_final.csv`                       |
| `regional_TDABM.ipynb`    | `regional_features_final.csv`                       |
| `replacement_ratio.ipynb` | `regional_replacement_ratio.csv`, `sectoral_replacement_ratio.csv` |


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

