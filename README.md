# nginx-host-config
Eases templating and management for nginx configs in the order of 100's

```
Usage: hostconfig [OPTIONS] COMMAND <hostname_pattern> [SETTINGS]
       hostconfig [ -h | --help ]

Crowded utility for confd template (nginx config) management.

Options:
  -h, --help            Print usage
  -c  --config=file     Supply custom config file location
  -f, --force           Override safety guards for some operations
  -s, --sync-only       No checks/reloads for dry run or when no nginx installed
  -t, --template=path   Override the default template
  -p, --primary=host    Specify primary hostname to use
  -e, --exact           Use with -p for hostname_pattern without default extra hosts

Settings (left-hand side is default):
  --stdhost || --barehost   Config with/without redirects, extra hostnames, etc
  --listed  || --unlisted   A listed/unlisted(hidden) config (SEO etc.)
  --https   || --http       Render a http(only)/https config
  --enable  || --disable    Enable/disable config in nginx

Commands:
    new         Use to create a new site
    update      Update an existing site
    update-all  Update all existing sites
    delete      Delete an existing site
```