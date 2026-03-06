# better checkout

composite action that:

- creates a github app token ([`actions/create-github-app-token`](https://github.com/actions/create-github-app-token)) (optional)
- checks out the repository ([`actions/checkout`](https://github.com/actions/checkout))
- sets the git `user.name` and `user.email`

works for github, gitea & forgejo actions

## Usage

```yaml
- id: checkout
  name: Checkout
  uses: spotdemo4/better-checkout@v0.5.0
  with:
    token: ${{ secrets.TOKEN }}
    # or
    app-id: ${{ vars.APP_ID }}
    private-key: ${{ secrets.PRIVATE_KEY }}
```

## Inputs

### `token`

checkout token

### `app-id`

github app client id

### `private-key`

github app private key

### `ref`

git ref to checkout

### `fetch-depth`

depth for git fetch

### `submodules`

whether to checkout submodules

### `path`

path to checkout repo

## Outputs

### `platform`

git platform (`github`/`gitea`/`forgejo`)

### `os`

runner operating system (`linux`/`darwin`/`windows`)

### `arch`

runner architecture (`amd64`/`arm64`/`arm`/`386`)

### `token`

github app token

### `name`

git user name

### `email`

git user email
