# `rubicon` notebooks

The `rubicon` notebooks are interactive versions of the examples found in our
documentation. You can clone the repo and run the examples on your own, or just
take a look at their outputs here!

### Running the notebooks

To ensure these examples work with your version of `rubicon`, clone this repository
at the tag corresponding to the verison of `rubicon` you'll be using by replacing
`X.X.X` in the command below with that version.

```
git clone https://github.com/capitalone/rubicon.git --branch X.X.X --single-branch
```

Then, create and activate the `conda` environment in the `notebooks` directory.

```
cd rubicon
conda env create -f notebooks/user-environment.yml
conda activate rubicon
```

The example notebooks can be viewed with either the `jupyter notebook` or `lab`
command.

```
jupyter notebook notebooks/
```

```
jupyter lab noteboooks/
```

**Note**: The first time you use JupyterLab you should be prompted to re-build
in order to install the extensions needed for our dashboard. If you are not
prompted or the dashboard is not working within JupyterLab, you can manually
re-build with:

```
jupyter lab build
```

### Development

When developing `rubicon` exmples, make sure to commit any notebooks with their
cells executed in order. These example notebooks are rendered as-is within the
[documentation](https://capitalone.github.io/rubicon/examples.html).

To developing examples off the latest on the `main` branch, use the `rubicon-dev`
environment in `environment.yml` at the root of the `rubicon` repository.

```
conda env create -f environment.yml
conda activate rubicon-dev
```

You'll need to install a local copy of the `rubicon` library as well.

```
pip install -e .[all]
```