.. _cpt_tracer:

Tracer
===============

The CernVM-FS client includes a tracer which will log FUSE calls
accessing the file system. In particular the following operations are being 
logged:

- `lookup`
- `open`
- `opendir`
- `statfs` and `getattr`
- `listxattr` and `getxattr`
- `readlink`

The tracer is activated by setting the `CVMFS_TRACEFILE` variable 
in the configuration file to the desired log file location.  
It is recommended to use the @fqrn@ variable in the trace log file in order to
distinguish operations accessing various repositories.  
It can be further configured through 
`CVMFS_TRACEBUFFER` and `CVMFS_TRACEBUFFER_THRESHOLD`.  
  
Please note that the Tracer might slow down the performance of CernVM-FS 
if activated. Any call to the file system blocks if the 
tracebuffer is full and underway of being flushed.  
The tracer functionality spawns one additional thread for
log writing upon activation.
