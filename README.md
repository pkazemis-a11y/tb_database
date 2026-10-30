# Tall buildings with diagrids: design exploration and assessment of the influence of the architectural form on the structural behavior

[![DOI](https://img.shields.io/badge/DOI-10.1016%2Fj.istruc.2026.113161-blue)](https://doi.org/10.1016/j.istruc.2026.113161)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Dataset](https://img.shields.io/badge/Dataset-1000_buildings-orange)]()

This repository contains the database and visualizations supporting the research paper on parametric design exploration of tall buildings with outer diagrids. The database comprises 1,000 artificial tall building models subjected to seven ground motion signals from the NGA-West2 database, providing a comprehensive resource for AI-driven structural design and early-stage decision support in the architecture, engineering, and construction community.

## Companion Repository

The surrogate-model and optimisation code developed from this dataset is maintained separately in the repository 
[tb_surrogate](https://github.com/pkazemis-a11y/tb_surrogate). This repository remains focused on the dataset, reference documentation, and supporting visual material for the dataset paper.

## 📁 Repository Structure

```
├── data/                      # Raw datasets
│   └── database.csv          # Main parametric database (7000+ rows)
├── visualizations/           # Interactive analysis plots
│   ├── *.html               # Interactive HTML visualizations
│   └── README.md            # Visualization documentation
├── examples/                 # Example scripts
│   ├── load_data.py         # Python example for data loading
│   └── README.md            # Examples documentation
├── docs/                     # Documentation and resources
│   ├── DATASET.md           # Detailed dataset documentation
│   ├── METHODOLOGY.md       # Research methodology
│   ├── GETTING_STARTED.md   # Getting started guide
│   └── FAQ.md               # Frequently asked questions
├── CITATION.cff             # Citation information
├── CONTRIBUTING.md          # Contribution guidelines
├── CHANGELOG.md             # Version history
├── requirements.txt         # Python dependencies
├── LICENSE                  # Repository license
└── README.md                # This file
```

## 🚀 Getting Started

New to this dataset? Start here:

1. **[Getting Started Guide](docs/GETTING_STARTED.md)** - Quick start with code examples
2. **[Example Scripts](examples/)** - Ready-to-run Python examples
3. **[Dataset Documentation](docs/DATASET.md)** - Complete variable descriptions
4. **[Methodology](docs/METHODOLOGY.md)** - Research methodology and technical details
5. **[Visualizations](visualizations/README.md)** - Interactive plot documentation
6. **[FAQ](docs/FAQ.md)** - Frequently asked questions

### Quick Start

```bash
# Clone the repository
git clone https://github.com/pkazemis-a11y/tb_database.git
cd tb_database

# Install dependencies
pip install -r requirements.txt

# Run example analysis
cd examples
python load_data.py
```

## 📄 Abstract

Tall buildings with diagrids offer several advantages over alternative structural solutions, including the possibility of reducing the dimensions of interior cores and freeing up interior space. However, the interplay between structural systems and architectural form is not always adequately considered during the early stages of design to support quantitative decision-making. In this study, a database comprising 1000 tall buildings has been generated using parametric modeling. The buildings range in height from 140 to 300 meters. These buildings have then been subjected to seven ground motions selected from the NGA-West2 database, for a total of 7000 simulations. Data related to geometric, structural, and environmental variables will subsequently be processed to support investigations based on artificial intelligence-driven generative approaches aimed at producing alternative optimized solutions. In this paper, the data are described in terms of specific 22 input (10 architectural, 12 related to the ground motion) and 99 output (69 structural, 23 environmental, 7 geometry-dependent) features, demonstrating the extent to which the database has been expanded with respect to the original design space. The dataset is made available through a repository for the architecture, engineering, and construction community.

## ✨ Highlights

- Detailed workflow for the numerical generation of a tall building database.
- Database of 1000 tall buildings with diagrids available online.
- Seismic analysis in the time domain for seven moderate earthquakes.
- Assessment of the influence of architectural form on structural behavior.
- Geometrical, structural, and environmental features, including cost and carbon footprint.

## 📊 Dataset Overview

The database advances previous work by:
- **Creating and managing 1000 building forms** through automated numerical simulations, allowing for alternative vertical transformations along building height
- **Considering dynamic response** under moderate seismic excitation with transient analyses in the time domain using 7 input ground accelerometers
- **Organizing data** for AI/ML applications, with accurate management of input file generation, output definition, technical procedures for computer cluster analyses, and data storage

### Main Database: `database.csv`
- **Records**: 1,000 building models × 7 ground motions = 7,000+ rows
- **Design Variables (X1-X10)**:
  - X1: Top plan geometry side count (3-12 sided polygons)
  - X2: Bottom plan geometry side count (3-12 sided polygons)
  - X3: Top/Bottom plan orientation
  - X4: Number of stories
  - X5: Floor height
  - X6: Vertical transformation method
  - X7: Tapering ratio (includes tapered forms)
  - X8: Twisting angle (allows twisting along building height)
  - X9: Curvilinear; location of control floor (includes curvilinear forms)
  - X10: Curvilinear; scale of control floor

- **Structural Outputs**: Mass, displacements, stresses, drift ratios, torsion
- **Seismic Inputs**: 7 NGA-West2 ground motions with characteristics
- **Economic Data**: Construction costs (structure, floor, land), sellable price

## 📈 Visualizations

Interactive HTML visualizations are organized into two categories:

### Ground Motion 1 (Single GM Analysis)
- Height vs Tapering Ratio
- Height vs Twisting Angle
- Maximum inter-storey drift vs height
- Plan side ratio vs twisting angle

### All Ground Motions (Comparative Analysis)
- Maximum acceleration vs height
- Maximum building displacement vs height
- Maximum inter-storey drift vs height
- Von Mises stress vs height (by drift and earthquake)

## 🔍 Key Variables

| Category | Variables |
|----------|-----------|
| **Geometric** | Plan geometry, orientation, height, tapering, twisting, curvilinearity |
| **Structural** | Mass, diagrid angles, stresses (tension, compression, shear), von Mises |
| **Seismic Response** | Acceleration, displacement, inter-storey drift, torsion, reactions |
| **Economic** | Material costs, structural costs, land costs, total costs/area |
| **Ground Motion** | NGA-West2 ground motion characteristics |

## 💻 Usage

This dataset is suitable for:
- **Classification or regression** tasks in structural design
- **Training artificial neural networks** or generative adversarial networks
- **Implementing generative design strategies** for tall buildings
- **Parametric sensitivity analysis** of architectural forms
- **Early-stage design decision support** with quantitative structural feedback
- **Structural performance evaluation** under seismic loads
- **Cost-benefit analysis** considering structural behavior, construction costs, and embodied carbon footprint

The data organization supports subsequent investigations using artificial intelligence algorithms, enabling designers to receive rigorous feedback without addressing the onerous task of numerical computation.

## 📚 Ground Motion Data
- **Source**: NGA-West2 database
- **Count**: 7 ground motion records
- **Analysis**: Transient analyses in time domain (linear behaviour assumed)

## 🔮 Future Developments

The robustness of the procedure allows for future extensions:
- Different types of loads (e.g., wind load)
- Material nonlinearity considerations
- Expansion of database size with additional earthquakes
- Additional geometrical characteristics
- Analysis of features extracted from time series (beyond maxima)
- Connection to AI tools enabling verbal prompts for structural feedback

## 👥 Authors

- **Pooyan Kazemi** (Corresponding author) - seyedpooyan.kazemi@polimi.it
- **Alireza Entezami** - alireza.entezami@polimi.it
- **Michela Turrin**
- **Charalampos Andriotis**
- **Stefano Mariani** - stefano.mariani@polimi.it
- **Aldo Ghisi** - aldo.ghisi@polimi.it

*Department of Civil and Environmental Engineering, Politecnico di Milano, Piazza Leonardo da Vinci 32, 20133 Milano, Italy*

## ⚖️ License
See [LICENSE](LICENSE) for details.

## 📝 Citation

If you use this dataset in your research, please cite:

```bibtex
@article{kazemi2026diagrids,
  title={Tall buildings with diagrids: design exploration and assessment of the influence of the architectural form on the structural behavior},
  author={Kazemi, Pooyan and Entezami, Alireza and Turrin, Michela and Andriotis, Charalampos and Mariani, Stefano and Ghisi, Aldo},
  journal={Structures},
  volume={93},
  pages={113161},
  year={2026},
  issn={2352-0124},
  doi={10.1016/j.istruc.2026.113161},
  url={https://www.sciencedirect.com/science/article/pii/S2352012426021119}
}
```

**Paper DOI**: [10.1016/j.istruc.2026.113161](https://doi.org/10.1016/j.istruc.2026.113161)

## 📧 Contact

For questions, issues, or collaboration inquiries, please:
- Open a GitHub issue
- Contact the corresponding author: Pooyan Kazemi (seyedpooyan.kazemi@polimi.it)

## 🙏 Acknowledgments

This research was conducted at the Department of Civil and Environmental Engineering, Politecnico di Milano. The ground motion data is sourced from the NGA-West2 database.

---

**Keywords**: AI in building design • High-rise buildings • Diagrid • Structural database
