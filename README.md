# Energy System Uncertainty Catalog

A structured catalog of uncertainties for energy-system modelling, covering **parametric, structural, and temporal uncertainties** across renewable energy, heat, bioenergy, Power-to-X/hydrogen, storage, imports, grid infrastructure, and demand sectors.

The catalog is designed to support **uncertainty analysis, sensitivity analysis, scenario development, and model robustness assessment** in integrated energy-system models.

## Overview

Energy-system models are affected by multiple sources of uncertainty, including uncertain technology costs and potentials, modelling assumptions, system constraints, demand evolution, and weather-dependent time series. However, these uncertainties are often treated inconsistently across studies.

This repository provides a structured and traceable catalog of relevant uncertainty parameters that can be used to systematically identify and characterize uncertainty in energy-system models.

The catalog distinguishes between three main uncertainty classes:

* **Parametric uncertainty** — uncertainty in numerical model inputs such as investment costs, technology efficiencies, capacities, potentials, and technical parameters.
* **Structural uncertainty** — uncertainty arising from modelling choices, system representation, constraints, optimization assumptions, and technology inclusion/exclusion.
* **Temporal uncertainty** — uncertainty associated with weather years, demand profiles, time series, and other time-dependent model inputs.

## Catalog Structure

The main catalog is provided as an Excel workbook:

`Uncertainty Catalog.xlsx`

The workbook contains the following sheets:

### `Main`

Provides an overview of the uncertainty classification and technology categories used throughout the catalog.

### `Parametric`

Contains numerical model parameters and their associated uncertainty ranges.

Each parameter includes information such as:

| Field                   | Description                                  |
| ----------------------- | -------------------------------------------- |
| ID                      | Unique uncertainty identifier                |
| Parameter               | Parameter name                               |
| Technology Category     | Relevant technology or sector                |
| Model Component         | Specific model component                     |
| Sector                  | Electricity, heat, gas, etc.                 |
| Unit                    | Parameter unit                               |
| Baseline                | Reference value                              |
| Lower Bound             | Lower uncertainty boundary                   |
| Upper Bound             | Upper uncertainty boundary                   |
| Uncertainty Type        | Epistemic, aleatory, or mixed                |
| Reference Plot          | Location of supporting reference data        |
| Source / Reference      | Literature and data sources                  |
| Justification           | Rationale for the selected uncertainty range |
| Description             | Interpretation of the parameter              |
| Parameter Name in Model | Corresponding model variable                 |

### `Structural`

Contains uncertainties associated with the formulation and structure of the energy-system model.

Examples include:

* Temporal resolution
* CO₂ constraints
* Grid losses
* Storage operating assumptions
* Optimization approach
* Penalty costs
* Technology inclusion/exclusion
* Alternative system configurations

### `Temporal`

Contains uncertainties related to time-dependent inputs and scenarios, including:

* Wind generation profiles
* Rooftop PV profiles
* Open-field PV profiles
* Solar-thermal generation
* Electricity demand
* Heat demand
* Gas demand

The catalog distinguishes between **aleatory uncertainty**, such as interannual weather variability, and **mixed uncertainty**, where both variability and modelling assumptions contribute.

### `Sources`

Contains the literature and other sources used to derive or justify the uncertainty ranges.

### `Reference plot`

Contains the reference information used to derive selected numerical uncertainty ranges for technology parameters.

## Technology and Sector Coverage

The catalog currently covers uncertainty parameters across several major areas of integrated energy-system modelling:

* Renewable energy
  * Rooftop photovoltaic systems
  * Open-field photovoltaic systems
  * Onshore wind
  * Hydropower
  * Solar thermal
* Heat systems
* Bioenergy
* Power-to-X and hydrogen
* Storage technologies
* Imports
* Grid infrastructure
* Electricity, heat and gas demand
* General simulation and optimization assumptions

## Uncertainty Classification

The catalog follows a distinction between **epistemic, aleatory, and mixed uncertainty**.

### Epistemic uncertainty

Uncertainty resulting from incomplete knowledge, limited data, uncertain future technology development, or uncertain parameter estimates.

Examples include:

* Technology investment costs
* Technology efficiencies
* Renewable energy potentials
* Grid parameters
* Storage parameters

### Aleatory uncertainty

Variability inherent to the system or its external conditions.

Examples include:

* Weather conditions
* Renewable generation profiles
* Interannual variability
* Time-dependent resource availability

### Mixed uncertainty

Parameters for which both knowledge uncertainty and inherent variability are relevant.

Examples include:

* Demand development
* Weather-dependent demand
* Model structure
* Optimization assumptions

## Intended Use

The catalog can be used as a starting point for:

1. **Global sensitivity analysis**
2. **Sobol analysis**
3. **Monte Carlo simulations**
4. **Uncertainty propagation**
5. **Scenario generation**
6. **Robustness analysis**
7. **Model comparison**
8. **Identification of influential parameters**
9. **Reduction of large parameter spaces**
10. **Systematic documentation of modelling assumptions**

A particular focus is enabling researchers to move from a large initial uncertainty space toward a smaller set of **highly influential parameters** for computationally expensive sensitivity analyses.

## Parameter Traceability

Where possible, each uncertainty parameter is linked directly to its corresponding model variable or implementation.

For example:

```text
Parameter
    ↓
Technology / Model Component
    ↓
Baseline value
    ↓
Lower / Upper uncertainty bound
    ↓
Uncertainty classification
    ↓
Literature / data source
    ↓
Model parameter
```

This provides a traceable connection between the uncertainty identified in the literature and its implementation within an energy-system model.

## Data Sources

The catalog draws on published literature, energy-system studies, technology reports, and other publicly available sources.

The `Sources` sheet provides the corresponding references for the parameter definitions and uncertainty ranges. As an example the catalogue is built on the Thuringia Energy system model and display for the year 2045. The value for other years can be obtained formt eh reference plots. 

## Scope and Limitations

This catalog should be considered a **living research resource rather than a definitive database of uncertainty ranges**.

Uncertainty ranges can depend on:

* Geographic scope
* Model boundaries
* Technology definition
* Reference year
* Scenario assumptions
* Data source
* Technology maturity
* Method used to derive the range

Therefore, users should assess the applicability of each parameter and its uncertainty range to their specific modelling framework before applying it.

## Citation

If you use this catalog in academic research, please cite the repository and the underlying sources listed in the `Sources` sheet.

A formal citation will be added once the associated research publication is available.

## Contributing

Contributions are welcome.

Potential contributions include:

* Additional uncertainty parameters
* New technologies
* Updated uncertainty ranges
* Additional literature sources
* Improved parameter classifications
* Corrections to existing entries
* Model-specific parameter mappings

When adding or modifying an uncertainty parameter, please provide the corresponding source and a clear justification for the selected uncertainty range.

## License

The Uncertainty Catalog is licensed under the Creative Commons Attribution 4.0 International License (CC BY 4.0).

You are free to share and adapt the catalog, including for commercial purposes, provided that appropriate credit is given to the original authors and any changes are indicated.

License: Creative Commons Attribution 4.0 International (CC BY 4.0)

Please cite this repository and the associated publication when using the catalog in academic or other research work.

Important: The license applies to the original material contained in this repository. Third-party data, publications, figures, or other externally sourced material remain subject to their respective licenses and copyright conditions.

## Citation

If you use this catalog in your research, please cite:


