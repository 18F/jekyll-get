# Install

Add this file to `_plugins` in the root of your Jekyll site.

# Configure

This plugin reads settings from the `_config.yml` file. Add settings as attributes or an array of attributes for multiple files.

## Example

```yml
jekyll_get:
  data: team
  json: 'https://18f.gsa.gov/hub/api/team/'
```

Or

```yml
jekyll_get:
  - data: team
    json: 'https://18f.gsa.gov/hub/api/team/'
  - data: projects
    json: 'https://18f.gsa.gov/hub/api/projects/'
```

Use in a liquid template as if it were a local data file:

```liquid
{% for member in site.data.team %}
  Hello {{member[1].first_name}}
{% endfor %}
```