# Jdaviz Profiler Usecases

This repository contains Jdaviz Profiler's use cases.
The use cases are organized in the `usecases` directory, and each use case is contained in its own subdirectory.
Each use case subdirectory contains a Jupyter notebook template and a parameters file to be used by the Jdaviz Profiler to generate and profile the use case.

Link to the [Jdaviz Profiler repository](https://github.com/spacetelescope/jdaviz_profiler).

## How to build a new use case

The `template.ipynb` file serves as the base notebook, while `params.json` contains the parameter values to be injected into the notebook.

The `template.ipynb` must have a cell with placeholders for the parameters to be replaced, therefore this cell must:
- precede all other cells with actual code using the parameters.
- be tagged with the `parameters` label.

Each parameter in the params.json file must have a corresponding placeholder in the template.ipynb file, and the placeholders must be unique having `_value` as suffix, e.g. `image_pixel_side_value` or `viewport_pixel_size_value` correspond to `image_pixel_side` or `viewport_pixel_size` parameter value used in the `template.ipynb`.

The generated parameterized notebooks will be saved in the `usecases/<usecase path>/notebooks` directory.

An example of how to structure a new `<usecase>` (along with `template.ipynb` and `params.json` files) is provided in this repository in `imviz_images`.

The Jdaviz Profiler has a script to create a new use case from the template.
