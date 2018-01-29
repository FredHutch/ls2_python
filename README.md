# ls2_python


Please look at [ls2](https://github.com/FredHutch/ls2) for details on how to build these Dockerfiles and how to use them to deploy the same software to a local archive.

This container adds:

* Life Sciences Software that does not require R, Python or Perl

## Build Software

Use `docker build . --tag ls2_tools` to build the container.

## Interactive Use
The default command runs EasyBuild to build all the packages defined in easyconfigs.  The easybuild command can be commentened out of the Dockerfile to allow interactive building of easyconfig files.

Interactive use: `docker run -it  --name ls2_tools --user neo ls2_tools /bin/bash`

Setup Easybuild environment:

```source /home/neo/.local/lmod/lmod/init/bash
module use /home/neo/.local/easybuild/modules/all
module load R/3.4.3-foss-2016b-fh2```
