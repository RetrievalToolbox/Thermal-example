# Installation and Running the Example

From within the cloned directory:

    julia --project=. -e 'using Pkg; Pkg.instantiate()'

Install XRTM according to the [RetrievalToolbox installation guide](https://github.com/US-GHG-Center/RetrievalToolbox.jl).

Then to launch a Jupyter notebook

    XRTM_PATH=/path/to/xrtm julia --project=. -e 'using IJulia; notebook(dir=pwd())'

On the first ever execution of the command above, users will likely be prompted to install Jupyter via the Julia/Conda module. After doing so, a fresh browser window should appear with the file browser looking at the project directory. From there, just open the `MWE-thermal.ipynb` file and click through the cells in the example notebook.