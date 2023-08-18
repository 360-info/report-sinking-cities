# Sinking cities

Visualises the measured land subsistence (sinking) across dozens of coastal cities.

## Use + Remix rights

![[Creative Commons Attribution 4.0](https://creativecommons.org/licenses/by/4.0)](https://mirrors.creativecommons.org/presskit/buttons/80x15/png/by.png)

These charts, as well as the analyses that underpin them, are available under a Creative Commons Attribution 4.0 licence. This includes commercial reuse and derivates.

<!-- Do any of the data sources fall under a different licence? If so, describe the licence and which parts of the data fall under it here! if most of it does, change the above and replace LICENCE.md too -->

Data in these charts comes from:

* [Tay et al. (2002)](10.1038/s41893-022-00947-z): Sea-level rise from land subsidence in major coastal cities
  - [Replication data for Tay at al. (2022)](https://researchdata.ntu.edu.sg/dataset.xhtml?persistentId=doi:10.21979/N9/GPVX0F) is freely available and is required to reproduce the analysis here.

## 📁 Ready to use data

Processed data for this map is available in the [`/data`](data) folder.

**Please attribute 360info and Tay et al. (2022) when you use and remix these visualisations.**

## Reproduce the analysis

### 💨 Quickstart: use the dev container

This project comes with a ready-to-use [dev container](https://code.visualstudio.com/docs/remote/containers) that includes everything you need to reproduce the analysis (or do a similar one of your own!), including [R](https://r-project.org) and [Quarto](https://quarto.org).

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/360-info/report-sinking-cities)

If you have Docker installed, you can also build and run the container locally:

  - Download or clone the project
  - Open it in [Visual Studio Code](https://code.visualstudio.com)
  - Run the **Remote-Containers: Reopen in Container** command

Once the container has launched (it might take a few minutes to set up the first time), you can run the analysis scripts with:

```sh
quarto render
```

Or look for the `.qmd` files to modify the analysis.

### Manual setup

To setup a development environment manually, 

You'll need to:
- [Download and install Quarto](https://quarto.org/docs/get-started)
- [Download the install R](https://www.r-project.org)
- Satisfy the R package dependencies. In R:
  * Install the [`renv`](https://rstudio.github.io/renv) package with `install.packages("renv")`,
  * Then run `renv::restore()` to install the R package dependencies.
  * (For problems satisfying R package dependencies, refer to [Quarto's documentation on virtual environments](https://quarto.org/docs/projects/virtual-environments.html).)

Now, render the `.qmd` files to the `/out` directory with:

```sh
quarto render
```

## ❓ Help

If you find any problems with our analysis or charts, please feel free to [create an issue](https://github.com/360-info/report-sinking-cities/issues/new)!
