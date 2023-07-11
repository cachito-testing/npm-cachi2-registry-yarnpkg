# npm-cachi2-registry-yarnpkg

Repo for testing yarn registry with npm package.

See the lockfile-v1 and lockfile-v3 branches for lockfileVersion specific tests.

## Package creation
```shell
podman run --rm -ti -v "$PWD:$PWD:z" -w "$PWD" --user 0 \
  registry.access.redhat.com/ubi7/nodejs-14 bash    # for npm v6
podman run --rm -ti -v "$PWD:$PWD:z" -w "$PWD" --user 0 \
  registry.access.redhat.com/ubi9/nodejs-18 bash    # for npm v9

npm install --global yarn
yarn --version
yarn install
npm install -g synp
synp -s yarn.lock
npm install
```
