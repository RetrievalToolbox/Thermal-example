# Installation and Running the Example

From within the cloned directory:

    julia --project=. -e 'using Pkg; Pkg.instantiate()'

This installs the required modules, including the RetrievalToolbox library itself. Note that this repository shows an example related to the thermal spectral range, which as of April 2026 is not yet integrated into the main branch. Thus, if users want to instantiate a project environment manually, they need to access the `#thermal` branch of RetrievalToolbox when adding the module:

    julia> using Pkg
    julia> Pkg.add(url="https://github.com/US-GHG-Center/RetrievalToolbox.jl#thermal")

Install XRTM according to the [RetrievalToolbox installation guide](https://github.com/US-GHG-Center/RetrievalToolbox.jl). The needed functionality for thermal wavelength ranges, i.e. the handling of isotropically emitted radiance from both the surface as well as the atmosphere itself, is handled only via XRTM (for the time being). Integrated Beer-Lambert solver for absorption-only atmospheres *does not yet support thermal emission*.

Then to launch a Jupyter notebook

    XRTM_PATH=/path/to/xrtm julia --project=. -e 'using IJulia; notebook(dir=pwd())'

On the first ever execution of the command above, users will likely be prompted to install Jupyter via the Julia/Conda module. After doing so, a fresh browser window should appear with the file browser looking at the project directory. From there, just open the `MWE-thermal.ipynb` file and click through the cells in the example notebook.

Note that downloading and building the spectroscopy file may take a few minutes. The resulting spectroscopy table will automatically be saved for later on, so re-running the example will skip that portion unless the file is no longer present.