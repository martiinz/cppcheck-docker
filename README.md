# cppcheck-docker

Docker image for cppcheck - a static analysis tool for C++

See <http://cppcheck.sourceforge.net>

This docker image might be useful for continuous integration scenarios
where one does not want to install cppcheck on all slave nodes.

The docker repository can be found here: <https://hub.docker.com/r/stefanhudelmaier/cppcheck/>

# Available tags

* latest
* 1.71

# Usage

The directory with the source to be checked must be mounted as a volume under /src.
Parameters to cppcheck can be given after the image.

```
docker run -v $(pwd)/src:/src stefanhudelmaier/cppcheck \
	--enable=all --xml --xml-version=2 2> /tmp/cppcheck.xml
```
