# ParaSiF OpenFOAM(ESI)–FEniCSx Example

This repository contains **integrated test cases** demonstrating the coupling between the ParaSiF OpenFOAM (ESI) fluid solver and the ParaSiF FEniCSx structure solver.
It is maintained as a **submodule** of the main ParaSiF repository: [ParaSiF Main Repository](https://github.com/ParaSiF/ParaSiF).

---

## Overview

The ParaSiF OpenFOAM(ESI)–FEniCSx Example provides **basic coupled simulations** to test the functionality of fluid–structure interaction within the ParaSiF framework.

Key features:

- Verifies that **two-way partitioned coupling** between OpenFOAM (ESI) and FEniCSx works correctly.
- Provides a simple setup to test the ParaSiF workflow.
- Designed for **integration testing only** — it is *not* a scientific validation case.
- Useful for debugging coupling issues before applying to real benchmark or production problems.

---

## Compatible Codebases

The test cases has been tested and is compatible with the following versions:

- **[OpenFOAM v2506](https://www.openfoam.com/news/main-news/openfoam-v2506)**
- **[FEniCSx v0.9.0](https://github.com/FEniCS/dolfinx/releases/tag/v0.9.0.post1)**

> Users are recommended to use the above versions of codes to ensure full compatibility with ParaSiF solvers.

You must also have the corresponding ParaSiF submodules installed:

- [ParaSiF_OpenFOAM_ESI](https://github.com/ParaSiF/ParaSiF_OpenFOAM_ESI_Fluid_Submodule)
- [ParaSiF_FEniCSx](https://github.com/ParaSiF/ParaSiF_FEniCSx_Structure_Submodule)

---

## Location in the Main ParaSiF Repository

`ParaSiF/example/OpenFOAM_FEniCSx/`

---

## Repository Structure

```
ParaSiF/example/OpenFOAM_FEniCSx/
├── doc/                     # Folder for documentation and notes
└── example_cases/           # Coupled example cases
  ├── fsiBeam_pimpleFSIFoam  # Example case with single phase
  └── fsiBeam_interFSIFoam   # Example case with multiphase

```

---

## Installation

**Note:** This submodule does not require additional compilation. Follow the main ParaSiF repository instructions to initialise and install MUI, FEniCSx and OpenFOAM_ESI submodules and install other global dependencies if applicable.

## Running Example Cases

Example cases are located in the example_cases/ folder:

To run an example:

1. Navigate to one of the example case directories, e.g.:

```bash
cd example_cases/XXX
```

2. Source essential environments:

- If FEniCSx is installed under Spack, activate the relevant Spack environment.

- Export the PYTHONPATH to include the MUI Python wrapper.

- Source the OpenFOAM environment:

```bash
source /path/to/OpenFOAM/etc/bashrc
```

3. Run the coupled simulation:

```bash
./Allrun.sh
```

4. (Optional) Clean up previous results before rerunning:

```bash
./Allclean.sh
```

4. Check results:

During runtime, a `runData/` folder will be automatically generated to store the solver output (fluid Domain outputs, structure Domain outputs, general log files, etc.).

## Notes

These examples are not validation cases. They are provided only to confirm that coupling between OpenFOAM (ESI) and FEniCSx works correctly.

---

## Contributing

ParaSiF, including this submodule, is an **open-source project**, and contributions from the community are warmly welcomed.

There are many ways you can help improve this submodule, including:

- Adding new features, libs or solvers
- Improving documentation, tests and examples
- Fixing bugs or refining existing functionality
- Sharing feedback and suggestions for enhancements

Your contributions, whether large or small, are highly valued and help make ParaSiF a stronger resource for the research community.

For detailed guidance on contributing, please see the [CONTRIBUTING.md](https://github.com/ParaSiF/ParaSiF/blob/main/CONTRIBUTING.md) in the main ParaSiF repository.

---

## License

Copyright (C) 2021–2025 The ParaSiF Development Team.  
Licensed under the **GNU General Public License v3 (GPL-3.0)**.

---

## Contact

For questions or contributions, please contact the ParaSiF Development Team
