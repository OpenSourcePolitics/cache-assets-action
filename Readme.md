# Cache precompile action

This action caches the precompile assets of your Rails application.
It is useful to speed up the tests suite of your application.

## Inputs

* key:
  - description: 'Cache key name'
  - required: false
  - default: assets-cache-${{ runner.os }}-${{ github.ref }}
* path:
  - description: 'A list of files, directories, and wildcard patterns to cache and restore'
  - required: false
  - default:
    - public/packs-test
    - tmp/webpacker-cache

## Usage

To use this action, you need to add the following step to your workflow:
```yaml
- uses: decidim/decidim-cache-precompile-action@master
```
