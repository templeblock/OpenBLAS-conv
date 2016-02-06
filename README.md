This is a convolution implementation with on the fly Toeplitz matrix generation.
It's a derivative work of OpenBLAS and requires the full OpenBLAS, as only few OpenBLAS
routines have been modified, the rest (gemm kernels) is taken from OpenBLAS itself. It
has been tested on various flavours of Linux.

## Building

    make OPENBLASDIR=<OpenBLAS base installation directory>

## Installing

	make install OPENBLASDIR=<OpenBLAS base installation directory>
	
If no OPENBLASDIR is given, /opt/OpenBLAS is assumed.
This will install the library in the same place where OpenBLAS is installed. Since OpenBLAS is
installed in /opt/OpenBLAS by default and /opt/OpenBLAS/lib is not in the default search paths
for libraries, assure to have it set (e.g. export LD_LIBRARY_PATH=/opt/OpenBLAS/lib on Linux,
export DYLD_LIBRARY_PATH=/opt/OpenBLAS/lib on Mac).
