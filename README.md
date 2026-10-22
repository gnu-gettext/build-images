# Building images for building and testing GNU gettext

This gettext sub-project generates and pushes to ghcr.io
docker registry the docker images to be used for compiling the
master branch of gettext and gnulib.

The reason for pre-generating the images is to speed-up build runs
and avoid failures due to downloading of individual packages (e.g.,
because some mirrors were down).
