# jenkins

## Gathering installed plugins

```sh
unset password
read -s -r password
JENKINS_HOST="username:$password@host:port"

# query jenkins console for plugin list
curl -sSL "http://$JENKINS_HOST/pluginManager/api/xml?depth=1&xpath=/*/*/shortName|/*/*/version&wrapper=plugins" | perl -pe 's/.*?<shortName>([\w-]+).*?<version>([^<]+)()(<\/\w+>)+/\1 \2\n/g'|sed 's/ /:/'
```