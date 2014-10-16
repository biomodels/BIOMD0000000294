# BIOMD0000000294: restif07

## Installation

Download this repository, and install with distutils

`python setup.py install`

Or, install using pip

`pip install git+https://github.com/biomodels/BIOMD0000000294.git`

To install a specific version (in this example, from the 2014-09-16 BioModels release)

`pip install git+https://github.com/biomodels/BIOMD0000000294.git@20140916`

## Usage

Importing the model package.

`import BIOMD0000000294 as model`

Get the SBML string from the model

`print model.sbmlString`

If [python-libsbml](https://pypi.python.org/pypi/python-libsbml) bindings are
installed, the libsbml.SBMLDocument object is also accessible

`model.sbml`


# Model Notes


This is the model described in the article:  
**Vaccination and the dynamics of immune evasion. **   
Restif O, Grenfell BT. _J R Soc Interface._ 2007 Feb 22;4(12):143-53.
PMID:[17210532](http://www.ncbi.nlm.nih.gov/pubmed/17210532),
doi:[10.1098/rsif.2006.0167](http://dx.doi.org/10.1098/rsif.2006.0167);  
**Abstract:**   
Vaccines exert strong selective pressures on pathogens, favouring the spread
of antigenic variants. We propose a simple mathematical model to investigate
the dynamics of a novel pathogenic strain that emerges in a population where a
previous strain is maintained at low endemic level by a vaccine. We compare
three methods to assess the ability of the novel strain to invade and persist:
algebraic rate of invasion; deterministic dynamics; and stochastic dynamics.
These three techniques provide complementary predictions on the fate of the
system. In particular, we emphasize the importance of stochastic simulations,
which account for the possibility of extinctions of either strain. More
specifically, our model suggests that the probability of persistence of an
invasive strain (i) can be minimized for intermediate levels of vaccine cross-
protection (i.e. immune protection against the novel strain) and (ii) is lower
if cross-immunity acts through a reduced infectious period rather than through
reduced susceptibility.

This version of the model can be used for both the stochastic and the
deterministic simulations described in the article. For deterministic
interpretations with infinite population sizes, set the population size _N_ =
1. The model does reproduces the deterministic time course. The initial values
are set to the steady state values for a latent infection with strain 1 with
an invading infection of strain 2 (I2=1e-06), 100 percent vaccination with a
susceptibility reduction τ=0.7 at birth (p=1), and all other parameters as in
figure 3 of the publication.

To be compatible with older software tools, the english letter names instead
of the greek symbols were used for parameter names:  
parameter | symbol | name  
---|---|---  
transmission rate | β | beta  
recovery rate | γ | gamma  
birth/death rate | μ | mu  
rate of loss of natural immunity | σ | sigma  
rate of loss of vaccine immunity | σv | sigmaV  
reduction of susceptibility by primary infection | θ | theta  
reduction of infection period by primary infection | ν | nu  
reduction of susceptibility by vaccination | τ | tau  
reduction of infection period by vaccination | η | eta  
  
Originally created by libAntimony v1.4 (using libSBML 3.4.1)


