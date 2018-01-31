# What's New

v1.1.1 (7 February 2017

This release contains a number of bug and compatibility fixes.

### Enhancements

- Ability to pass a dictionary to top level RVIC functions (instead of only a file path). This allows for the generation of large ensembles of RVIC simulations in an interactive environment ([GH78](https://github.com/UW-Hydro/RVIC/pull/78)).

### Bug Fixes

- Fixed bug that in `tools/fraction2domain.bash` by using a temporary variable name ([GH88](https://github.com/UW-Hydro/RVIC/pull/88)).
- Fixed off-by-one error in `history.py` ([GH86](https://github.com/UW-Hydro/RVIC/pull/86)).

v1.1.0 (25 October 2015)

This release contains a number of bug and compatibility fixes.

### Enhancements

- Compatibility with Python 3.4 and 3.5 ([GH38](https://github.com/UW-Hydro/RVIC/pull/38)).
- Simplified multiprocessing in `parameters` which should improve stability ([GH60](https://github.com/UW-Hydro/RVIC/pull/60)).

### Bug Fixes

- Fixed bug that caused `REMAP=False` to fail ([GH60](https://github.com/UW-Hydro/RVIC/pull/60)).
- Improvements were made to the `SEARCH_FOR_CHANNEL` option in `parameters`.
- Fixed bug where last timestep of history output was not populated ([GH71](https://github.com/UW-Hydro/RVIC/pull/71)).
- `subset_length` cast as an int since it is used to initialize `out_uh` array in `param_file.py`.
- ValueError raised if `subset_length` is not a multiple of 2 before passing `subset_length` to `subset` function in `param_file.py`, since +/- `subset_length` / 2 is used to define `d_left` and `d_right`, which are in turn used as array indices.

