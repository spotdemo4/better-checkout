# better checkout

composite action that:

- creates a github app token via [actions/create-github-app-token](https://github.com/actions/create-github-app-token) (optional)
- checks out the repository via [actions/checkout](https://github.com/actions/checkout)
- sets the git `user.name` and `user.email`

works for github, gitea & forgejo

## Usage

```yaml
- uses: spotdemo4/better-checkout@v0.3.0
  id: checkout
  with:
    token: # ...
    app-id: ${{ vars.CLIENT_ID }}
    private-key: ${{ secrets.PRIVATE_KEY }}
    fetch-depth: # 0
```

## Inputs

### `token`

checkout token

### `app-id`

github app client id

### `private-key`

github app private key

### `fetch-depth`

depth for git fetch

### `submodules`

whether to checkout submodules

## Outputs

### `platform`

git platform (github/gitea/forgejo)

### `os`

runner operating system (linux/darwin/windows)

### `arch`

runner architecture (amd64/arm64/arm/386)

### `token`

github app token

### `name`

git user name

### `email`

git user email
