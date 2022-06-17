# Language Modeling 

This project contains a Bert-model on norwegian and the code to rebuild. Feel free to reuse it.

The model is in the data-directory. When checkout use Git lfs, as the file is pretty big.

## Why

This model works out of the box with f.eks. the sentence transfomer library.
It is built on top of the multilingual bert.

## Getting Started

```python

from sentence_transformers import SentenceTransformer
model = SentenceTransformer('checkpoint-33500')
vector =  model.encode("Ibsen er en norsk forfatter som ikke var redd for litt kinnskjegg..")


```

## Fine-tuning

Bert works best when fine tuned against the relevant material.

Put data in a directory and follow the train-part in the scripts here.


### Notebooks

To use your module code (`src/`) in Jupyter notebooks (`notebooks/`) without running into import errors, make sure to install the source locally

    pip install -e .

This way, you'll always use the latest version of your module code in your notebooks via `import language_modeling`.

Assuming you already have Jupyter installed, you can make your virtual environment available as a separate kernel by running:

    pip install ipykernel
    python -m ipykernel install --user --name="language-modeling"

Note that we mainly use notebooks for experiments, visualizations and reports. Every piece of functionality that is meant to be reused should go into module code and be imported into notebooks.

### Distribution Package

To build a distribution package (wheel), please use

    python setup.py dist

this will clean up the build folder and then run the `bdist_wheel` command.

### Contributions

Before contributing, please set up the pre-commit hooks to reduce errors and ensure consistency

    pip install -U pre-commit
    pre-commit install

## Contact

petter.egesund@sannsyn.com

Thanks to Russ and Wassim for cooperation :)

## License

Freebsd
