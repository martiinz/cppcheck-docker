# cppcheck-docker

Docker image for cppcheck - a static analysis tool for C++

See http://cppcheck.sourceforge.net

# Usage

The directory with the source to be checked must be mounted as a volume under /src.
Parameters to cppcheck can be given after the name of the image.

```
sudo docker run -v $(pwd)/src:/src cppcheck --enable=all --xml --xml-version=2 2> /tmp/test.xml
```
