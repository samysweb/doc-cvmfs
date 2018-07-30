.. _cpt_shrinkwrapping:

Shrinkwrapper
===============

The shrinkwrapping utility allows the export of a defined subset of files from
CVMFS to a POSIX folder or other formats (... TODO(steuber)).
For the subset specification the dirtab format described
:doc:`here </cpt-hpc.html#preloading-the-cernvm-fs-cache>` is used.

Use Case
---------------

The shrinkwrapper can be used in settings where one cannot or does not want to
rely on the availability of a (fast) internet connection allowing for an online
CVMFS Client.  
Typical usecases are benchmark workload container builds or container builds
for HPC sites (true? TODO(steuber)).

