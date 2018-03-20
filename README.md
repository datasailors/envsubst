# envsubst
Simple Docker container that provides the envsubst executable that can be used when expanding environment variables in strings or files.

## Example 1 - string

   docker container run --rm -it -e var=value iankoulski/envsubst sh -c "echo This container has \$var | envsubst"

output:

   This container has value

## Example 2 - file

   docker container run --rm -it -e var=value -v $(pwd):/wd iankoulski/envsubst sh -c "envsubst < /wd/file.txt > file-subst.txt" && cat file-subst.txt

output:

    This container has value

