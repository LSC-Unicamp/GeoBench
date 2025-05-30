# Miniwave - Minimum Simwave

Miniwave is a streamlined version of Simwave, tailored mainly for educational use and benchmarking of computational systems. Its backend implements only the wave propagation kernel (no absorbing layers, boundary conditions, etc). miniwave.py is a Python wrapper for the forward wave propagation.

`Simwave` is a Python package to simulate the propagation of the constant or variable density acoustic wave in an isotropic 2D/3D medium using the finite difference method. Finite difference kernels of aribtrary spatial order (up to 20th order) are written in C for performance and compiled at run time. These kernels are called via a user-friendly Python interface for easy integration with several scientific and engineering libraries to, for example perform full-waveform inversion.

For further information on the `simwave` design and implementation, please see the paper https://arxiv.org/abs/2201.05278

# Dependencies

`pip install numpy matplotlib findiff h5py`

```
mkdir /hdf5 && \
    cd /hdf5 && \
    wget https://support.hdfgroup.org/ftp/HDF5/releases/hdf5-1.14/hdf5-1.14.3/src/CMake-hdf5-1.14.3.tar.gz && \
    tar xf CMake-hdf5-1.14.3.tar.gz && \
    cd CMake-hdf5-1.14.3 && \
    ./build-unix.sh && \
    yes | ./HDF5-1.14.3-Linux.sh && \
    cp -r HDF5-1.14.3-Linux/HDF_Group/HDF5/1.14.3/ ../build
```

# How to use

`python3 miniwave.py --help`

`python3 miniwave.py --file FILE --grid_size GRID_SIZE --num_timesteps NUM_TIMESTEPS --language {c,openmp,openacc,cuda,python} --space_order SPACE_ORDER`

