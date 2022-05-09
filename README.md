# Windkessel model with power as input

**Tools and example data for simulating cardiac afterload with power as input to a Windkessel model**, using smoothed cubic splines to represent measured aortic pressure and flow signals and a differential-algebraic representation of the parallel 4-element Windkessel model.

The data and methods presented here were used to generate the results presented in the article "[The differential-algebraic Windkessel model with power as input](https://portal.research.lu.se/files/115310976/pigot2022differential.pdf)" by Henry Pigot and Kristian Soltesz, presented at the 2022 American Control Conference.

The code uses [DifferentialEquations](https://docs.juliahub.com/DifferentialEquations/UQdwS/6.15.0/), [CSV](https://csv.juliadata.org/stable/), [IJulia](https://julialang.github.io/IJulia.jl/stable/), [Plots.jl](https://github.com/JuliaPlots/Plots.jl), [Polynomials](https://juliamath.github.io/Polynomials.jl/stable/), [Sundials](https://diffeq.sciml.ai/stable/). Thank you to the developers behind those packages.

## Data

Aortic pressure and flow measurements [stergiopulos1999_data/](stergiopulos1999_data/) are from Figure 4A type A beat of [_Total Arterial Inertance as the Fourth Element of the Windkessel Model,_ Stergiopulos et al. (1999)](http://doi.org/10.1152/ajpheart.1999.276.1.H81), digitized using [Webplotdigitizer v4.4]({https://automeris.io/WebPlotDigitizer). Pressure in mmHg, flow in L/min.

## Getting started

1. Download [Julia](https://julialang.org/).
2. Install packages:
   1. Open Julia REPL, e.g. using the command `julia` in terminal,
   2. Enter the Pkg REPL by pressing ]
   3. add packages using command `add IJulia DifferentialEquations CSV Polynomials Sundials Plots`
3. Open a jupyter dashboard by running the command `notebook`
4. Navigate to the repo directory and open `power_windkessel.ipynb`, from there you can run the code

Note that this code was tested with `Julia 1.6.2` using the following package versions, in addition to the `Julia 1.6.2` standard libraries:

````sh
[7073ff75] IJulia v1.23.2
[0c46a032] DifferentialEquations v6.19.0
[336ed68f] CSV v0.9.2
[f27b6e38] Polynomials v1.2.1
[c3572dad] Sundials v4.5.3
[91a5bcdd] Plots v1.21.3
````
