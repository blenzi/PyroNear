# PyroNear
[![Donate](https://img.shields.io/badge/License-MIT-brightgreen.svg)](LICENSE) [![Codacy Badge](https://api.codacy.com/project/badge/Grade/55423de221b14b18a5e35804574d5d5a)](https://www.codacy.com/manual/fg/pyronear?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=frgfm/PyroNear&amp;utm_campaign=Badge_Grade)[![CircleCI](https://circleci.com/gh/frgfm/PyroNear.svg?style=shield)](https://circleci.com/gh/frgfm/PyroNear) [![codecov](https://codecov.io/gh/frgfm/PyroNear/branch/master/graph/badge.svg)](https://codecov.io/gh/frgfm/PyroNear) [![Docs](https://img.shields.io/badge/docs-available-blue.svg)](https://frgfm.github.io/PyroNear)

The increasing adoption of mobile phones have significantly shortened the duration between the beginning of a wildfire and the firefighting agents being alerted. In less dense areas, limiting and minimizing this amount of time is critical to preserve forest areas.

PyroNear aims at offering an wildfire early detection system with state-of-the-art performances at minimal deployment costs.



## Table of Contents

* [Getting Started](#getting-started)
  * [Prerequisites](#prerequisites)
  * [Installation](#installation)
* [Usage](#usage)
* [References](#references)
* [Documentation](#documentation)
* [Contributing](#contributing)
* [Credits](#credits)
* [License](#license)



## Getting started

### Prerequisites

- Python 3.6 (or more recent)
- [pip](https://pip.pypa.io/en/stable/)

### Installation

Use pip to install the package from git

```shell
pip install git+https://github.com/frgfm/PyroNear@master
```



## Usage

### datasets

Access all PyroNear datasets just like any `torchvision.datasets.VisionDataset`:

```python
from pyronear.datasets import OpenFire
dataset = OpenFire('./data', download=True)
```



## References

You are free to use any training script, but some are already provided for reference. In order to use them, install the specific requirements and check script options as follows:

```shell
pip install -r references/classification/fastai/requirements.txt
python references/classification/fastai/train.py --help
```

You can then run the script with your own arguments:

```shell
python references/classification/fastai/train.py --data-path ./data --lr 3e-3 --epochs 4 --pretrained --deterministic
```

*Please note that most tasks are provided with two training scripts (and their `requirements.txt`): one using [fastai](https://github.com/fastai/fastai) and the other without it.*



## Documentation

The full package documentation is available [here](<https://frgfm.github.io/PyroNear/>) for detailed specifications. The documentation was built with [Sphinx](sphinx-doc.org) using a [theme](github.com/readthedocs/sphinx_rtd_theme) provided by [Read the Docs](readthedocs.org).



## Contributing

Please refer to `CONTRIBUTING` if you wish to contribute to this project.



## Credits

This project is developed and maintained by the repo owner and volunteers from [Data for Good](https://dataforgood.fr/).



## License

Distributed under the MIT License. See `LICENSE` for more information.