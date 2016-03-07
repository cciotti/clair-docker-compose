# Analyze local images using clair
See: https://github.com/coreos/clair

This is a clunky initial docker-compose to work around some issues I had when running the analyze-local-images binary locally while running clair in a container.

## Running

1. `docker-compose up postgres` (and wait for postgres to startup)
2. In a separate terminal, `docker-compose up clair` (and wait for the initial update to happen, this can take several minutes)
3. In a separate terminal, `docker-compose run --rm analyze-local-images <imageid>

This will print out a list of CVEs for the local image you have selected.
