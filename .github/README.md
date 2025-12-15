# better checkout

composite action that checks out the repository and sets the git `user.name` and `user.email`

works for github, gitea & forgejo

## Usage

```yaml
- uses: spotdemo4/better-checkout@v0.0.2
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

github private key

### `fetch-depth`

depth for git fetch

## Outputs

### `token`

github app token

### `name`

git user name

### `email`

git user email
