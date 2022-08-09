# Update scs-frontend-config git repository
Updates the image tag of msp dev in scs-supercard-frontend-config repo

## Inputs

### `repository`

**Required** The frontend scs repository to update.

### `ref`

**Required** The branch to update.

### `token`

**Required** Token used for checkout.

### `docker-image-tag`

**Required** The image tag which should be written in the file.

### `stage`

**Required** The stage config file to update.

## Example usage

```
uses: interdiscount/github-actions-update-frontend-scs-repository@v1 
with:
    repository: interdiscount/scs-supercard-frontend-config
    ref: 'main'
    token: ${{ secrets.INTERDISCOUNT_COOP_USER_PW }}
    docker-image-tag: sha-${GITHUB_SHA::9}
    stage: development
```
