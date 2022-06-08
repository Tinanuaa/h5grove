# h5grove, core utilities to serve HDF5 file contents

**h5grove** is a Python package that provides utilities to design backends serving HDF5 file content: attributes, metadata and data. HDF5 files are accessed with [h5py](https://github.com/h5py/).

## Documentation

The documentation of the latest release is available [here](https://silx-kit.github.io/h5grove/).

## Rationale

There are several packages out there that can serve HDF5 files. However, they are dedicated to their usecases and settle on one implementation, hampering reusability.

In addition, some problems arise constantly when designing HDF5 backends. To name a few:

- Resolving external links
- Dealing with compression and slicing of datasets
- Encoding data efficiently and consistently (looking at you, `NaN`, `Infinity` in JSON)

**h5grove** aims at providing building blocks that solve these common problems and can be reused in existing or new backends.

## Installation

```bash
pip install h5grove
```

You can use **h5grove** low-level utilities whatever the backend implementation you choose. Additional utilities are provided for several Python web frameworks but require additional packages that can be installed the following way:

- [FastAPI](https://fastapi.tiangolo.com/)

```bash
pip install h5grove[fastapi]
```

- [Flask](https://flask.palletsprojects.com/en/)

```bash
pip install h5grove[flask]
```

- [Tornado](https://www.tornadoweb.org/en/stable/)

```bash
pip install h5grove[tornado]
```
