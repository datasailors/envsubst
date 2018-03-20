# envsubst
Simple Docker container that provides the envsubst executable that can be used when expanding environment variables in strings or files.

## Example

 docker run --rm -it -e var=value iankoulski/envsubst sh -c "echo This container has \$var | envsubst"

output:

This container has value

