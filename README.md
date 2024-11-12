# Radius Clustering

Radius clustering is a Python package that implements clustering under radius constraint based on the Minimum Dominating Set (MDS) problem. This problem is NP-Hard but has been studied in the literature and proven to be linked to the clustering under radius constraint problem (see [references](#references) for more details).

## Features

- Implements both exact and approximate MDS-based clustering algorithms
- Compatible with scikit-learn's API for clustering algorithms
- Supports radius-constrained clustering
- Provides options for exact and approximate solutions

## Installation

You can install Radius Clustering using pip:

```bash
pip install radius-clustering
```

> Note: This package is not yet available on PyPI. You may need to install it from the source.

## Usage

Here's a basic example of how to use Radius Clustering:

```python
import numpy as np
from radius_clustering import RadiusClustering

# Example usage
X = np.random.rand(100, 2)  # Generate random data

# Create an instance of MdsClustering
rad_clustering = RadiusClustering(manner="approx", threshold=0.5)

# Fit the model to the data
rad_clustering.fit(X)

# Get cluster labels
labels = rad_clustering.labels_

print(labels)
```

## Documentation

To build the documentation, you can run the following command, assuming you have Sphinx installed:

```bash
cd docs
make html
```

Then you can open the `index.html` file in the `build` directory to view the full documentation.

## More information

For more information please refer to the official documentation.

If you want insights on how the algorithm works, please refer to the [presentation](PRESENTATION.md).

If you want to know more about the experiments conducted with the package, please refer to the [experiments](EXPERIMENTS.md).


## Contributing

Contributions to MDS Clustering are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the GNU General Public License v3.0 - see the LICENSE file for details.


## Acknowledgments

### MDS Algorithms

The two MDS algorithms implemented are forked and modified (or rewritten) from the following authors:

- [Alejandra Casado](https://github.com/AlejandraCasado) for the minimum dominating set heuristic code [[1](https://www.sciencedirect.com/science/article/pii/S0378475422005055)], whom original code is available at [truc]. We rewrote the code in C++ to adapt to the need of python interfacing.
- [Hua Jiang](https://github.com/huajiang-ynu) for the minimum dominating set exact algorithm code [[2](https://dl.acm.org/doi/abs/10.24963/ijcai.2023/622)]. The code has been adapted to the need of python interfacing.

### Funders

The Radius Clustering work has been funded by:

- [LIAS, ISAE-ENSMA](https://www.lias-lab.fr/)
- LabCom @lienor and the [French National Research Agency](https://anr.fr/)

### Contributors

- Mickaël Baron, LIAS, ISAE-ENSMA
- Brice Chardin, LIAS, ISAE-ENSMA
- Quentin Haenn, LIAS, ISAE-ENSMA


## References

- [1] [An iterated greedy algorithm for finding the minimum dominating set in graphs](https://www.sciencedirect.com/science/article/pii/S0378475422005055)
- [2] [An exact algorithm for the minimum dominating set problem](https://dl.acm.org/doi/abs/10.24963/ijcai.2023/622)


