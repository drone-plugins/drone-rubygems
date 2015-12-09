Use this plugin for publishing gems to a Rubygems server. You can override the
default configuration with the following parameters:

* `api_key` - Rubygems API Key, get it [here](https://rubygems.org/profile/edit)
* `username` - Username, only required without API key
* `password` - Password, only required without API key
* `name` - Name of the gem, defaults to repo name
* `gemspec` - Path to gemspec, defaults to repo name with `.gemspec` suffix
* `host` - Rubygems host, only required for a selfhosted gem server
* `skip_cleanup` - Flag to deploy from the current file state

## Example

The following is a sample configuration in your .drone.yml file:

```yaml
deploy:
  rubygems:
    api_key: e123f83113f79eb17308bbf1ca8885bb
    when:
      branch: master
```
