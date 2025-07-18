# clumpy-LAMIR
Repository for clumped isotope data processing.
The purpose of this repository is to offer streamlined, open-source programs for processing and analyzing carbonate clumped isotope data.
This package is designed to standardize the data reduction process, ensuring that all operations (e.g., projection into the absolute reference frame (ARF), and standard correction, $\Delta_{48}$ excess handling) are performed in a unified way by all users in the community.

This is a modified version of [clumpy], for use in LAMIR Institute (Laboratório de Análise de Minerais e Rochas) of Universidade Federal do Paraná. 
Main changes from the original clumpy were made to adapt to our Isodat output data, which is slightly different from older versions of IRMS 253Plus.
Constants and calc parameters are being updated as new studies are published.

# Features
### 1. Isodat Parser (.did file processing)
The heart of this package is a parser that reads Isodat's proprietary data filed (.did files) at the 
binary level to extract useful data such as voltages, sample ID, and the Isodat-calculated bulk $\delta^{13}C$ and $\delta^{18}O$ values in standard reference frames.
This parser can run in manual mode, where the user imports single acquisition files in turn, specifying to which samples they belong,
or in automatic mode, where a block of acquisitions in a directiory are automatically parsed and divided into their likely samples.

### 2. Excel Parser
Reads in raw acquisiton data and sample names from a CIDS sheet with a Caltech-style format.
Useful for importing old data that has been processed in a special way.

### 3. The Clumped Isotope class (CI)
Class with associated methods for handling data obtained with either of the above parsers. Built with the class are functions 
for properly calculating more complicated clumped isotope parameters, such as $\Delta_{47}$ and $\Delta_{48}$.

# Requirements
* [Python 3]
* [numpy]
* [matplotlib]
* [xlrd]
* [scipy]

[Python 3]: https://www.python.org
[numpy]: https://numpy.org
[matplotlib]: https://matplotlib.org
[xlrd]: https://xlrd.readthedocs.io/
[scipy]: https://www.scipy.org
[clumpy]: https://github.com/maxmansaxman/clumpy


