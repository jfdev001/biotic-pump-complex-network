# biotic-pump-complex-network

Reproducing [Networks of forest ecosystems: Mathematical modeling of their biotic pump mechanism and resilience to certain patch deforestation](https://www.sciencedirect.com/science/article/pii/S1476945X20300386) as part of UvA's Complex System Simulation 2023 course.

The `notebooks` folder contains selected figures reproduced from the paper, the `src` contains functions for implementing the model, and the `scripts` folder contains a plotting and simulation file.

## Installation

Go to [julialang.org](https://julialang.org/downloads/).

*On Linux (this is the most stable setup, so please use this if possible):*

```
cd ~
wget https://julialang-s3.julialang.org/bin/linux/x64/1.9/julia-1.9.1-linux-x86_64.tar.gz
tar zxvf julia-1.9.1-linux-x86_64.tar.gz
```

Then edit your `~/.bashrc` file and add `export PATH="$PATH:~/julia-1.9.1/bin"`
to the end of the file. Note that you could replace the `~` in the path you
export to the `PATH` variable with `/home/<INSERT YOUR USERNAME>`. Finally,
`source ~/.bashrc` and then check to see that the Julia REPL works
by typing `julia`.

## Usage

If Julia is already installed, change to the directory of this project
and do the following in a command prompt:

```
julia> using Pkg
julia> Pkg.install("DrWatson") # only if not already installed
julia> Pkg.activate(".")
julia> Pkg.instantiate()
```

You may notice that Julia scripts start with the commands:

```julia
using DrWatson
@quickactivate :CSSim
```

which auto-activate the project and enable local path handling from DrWatson.

The above syntax is based on [making your DrWatson project a usable module](https://juliadynamics.github.io/DrWatson.jl/stable/real_world/#Making-your-project-a-usable-module-1),
which was done for the purposes of using `Revise.jl`. See the [discussion](https://discourse.julialang.org/t/best-debug-workflow-for-dr-watson/97234/5)
here for more information on this.

*For developers only:*

To setup `Revise.jl`, follow the instructions described [here](https://timholy.github.io/Revise.jl/stable/) and make sure
to modify your `~/.julia/config/startup.jl` to include `using Revise`.

# References

[Cantin2020](https://www.sciencedirect.com/science/article/pii/S1476945X20300386)

[Antonovsky1990](https://www.sciencedirect.com/science/article/abs/pii/004058099090043U?via%3Dihub)

[Julia Debugger.jl Tutorial](https://www.educative.io/answers/how-to-debug-script-in-julia)
