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

```
source /app/lmod/lmod/init/bash
module use /app/modules/all
module load EasyBuild```
