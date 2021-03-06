# wp-cli-media-restore

[![No Maintenance Intended](http://unmaintained.tech/badge.svg)](http://unmaintained.tech/)

Restore media attachments using WP CLI. Based on [download missing attachments](https://github.com/cftp/wp-cli-download-missing-attachments) with support for custom content directory and configuration in WP CLI config file.

## Installation

If you're using WP-CLI v0.23.0 or later, you can install this package with:

```
wp package install frozzare/wp-cli-media-restore
```

Or, using Composer directly:

```
composer require frozzare/wp-cli-media-restore
```

For other methods, please refer to WP-CLI's [Community Packages](https://github.com/wp-cli/wp-cli/wiki/Community-Packages) wiki.

## Config

Example of `~/.wp-cli/config.yml`:

```yaml
media:
  restore:
    generate: false
    uploads_url: http://www.bedrock.com/app/uploads/
```

## Options

#### `[--generate=false]`
Set this optional parameter if you want to (re)generate all the different image sizes. Defaults to not generating thumbnails.

#### `[--uploads-url]`
The URL to the uploads directory, not including any date based folder structure.

## Examples

```
wp media restore --uploads-url=http://www.bedrock.com/app/uploads/
```

## License

MIT © [Fredrik Forsmo](https://github.com/frozzare)
