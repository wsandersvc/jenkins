# jenkins

## Tools

### Maven
Add Maven via auto-install under tool configuration.

### JDK
**Note**: Set extracted path to the subpath containing the JDK bin folder. Typically the JDK version with Build Number.

## Clouds

### Docker Plugin
Docker plugin does not respect or support multi-platform builds. The environment variable DOCKER_DEFAULT_PLATFORM will not work. If a platform that is different from the Docker host's platform is required, use `FROM --platform=linux/amd64`.
Docker cloud defaults to host platform.