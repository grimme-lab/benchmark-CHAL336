# CHAL336 Benchmark Set

Benchmark set of non-covalent chalcogen bonding interaction energies.

## References

The reference values correspond to the values from the original publication of _Mehta, Fellowes, White, Goerigk_ (2021) and are obtained with the W1-F12 method or one of two DLPNO-CCSD(T)-based composite strategies (dubbed C and E in the paper), chosen per-system according to the procedure described therein.

The detailed procedure is described in _J. Chem. Theory Comput._, **2021**, _17_, 2783-2806 ([DOI](https://doi.org/10.1021/acs.jctc.1c00006)).
The geometries were taken from the original publication of CHAL336.

## Dataset Information
- **Systems**: 336 chalcogen-bonded complexation reactions across 1008 dimer/monomer-A/monomer-B geometries, split into four subsets:
  - `CHAL-CHAL-*` (99 reactions): chalcogen···chalcogen interactions.
  - `CHAL-N-*` (91 reactions): chalcogen···nitrogen interactions.
  - `CHAL-pi-*` (27 reactions): chalcogen···π interactions.
  - `CHAL-X-*` (119 reactions): chalcogen···halide interactions (charged systems).
- **Reference Level**: W1-F12 (for smaller systems) and DLPNO-CCSD(T)-based composite reference complexation energies in kcal/mol.
- **Geometries**: Located inside the `CHAL336/` folder, structured as standard `mol.xyz` files. Charges are specified in `.CHRG` files.
- **Evaluation**: The `.res` file contains reference complexation energies in kcal/mol. Use the [`tmer2++`](https://github.com/grimme-lab/tmer2) script to evaluate calculated energies against these references.

## Utils

The `.list` file is created via `find CHAL336 -maxdepth 1 -mindepth 1 -type d | sort > .list`.
