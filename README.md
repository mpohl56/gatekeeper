# Keycloak

Keycloak is an Open Source Identity and Access Management solution for modern Applications and Services.

Note:  This version of Keycloak Gatkeeper is modified from the project on the public github to make mutual TLS work properly.  There is a Docker release for this version on docker.io in the devsec2 repository.

This repository contains the source code for the Keycloak Gatekeeper. The Gatekeeper is most happy in the company of Keycloak, but is also able to make friends with other OpenID Connect providers. The service supports both access tokens in browser cookie or bearer tokens.

**Note:** This version of Keycloak-gatekeeper is modified from the version on the public web.  I hope to be allowed to send this to the open source project soon.  Until then, here is a list of the changes:

 * Modified the --tls-client-certificate option to really implement a client cert properly.  The internet version was setting the cert passed in with this parameter as the CA cert.
 * Added two command line options to deal with the CA cert for connecting from gatekeeper to Keycloak and adding a keyfile for the client certificate passed in with the --tls-client-certificate parameter.  
 * The new parameters are:  --tls-ca-server and --tls-client-key.

## Help and Documentation

* [Gatekeeper documentation](https://www.keycloak.org/docs/latest/securing_apps/index.html#_keycloak_generic_adapter)
* [Keycloak documentation](https://www.keycloak.org/documentation.html)
* [User Mailing List](https://lists.jboss.org/mailman/listinfo/keycloak-user) - Mailing list for help and general questions about Keycloak
* [JIRA](https://issues.jboss.org/projects/KEYCLOAK) - Issue tracker for bugs and feature requests


## Reporting Security Vulnerabilities

If you've found a security vulnerability, please look at the [instructions on how to properly report it](http://www.keycloak.org/security.html)


## Reporting an issue

If you believe you have discovered a defect in Gatekeeper please open an issue in our [Issue Tracker](https://issues.jboss.org/projects/KEYCLOAK).
Please remember to provide a good summary, description as well as steps to reproduce the issue.


## Getting started

To run Gatekeeper download the distribution from our [website](https://www.keycloak.org/downloads.html). Extract it and run:

    ./keycloak-gatekeeper[.exe]

Alternatively, you can use the Docker image by running:

    docker run -it --rm quay.io/keycloak/keycloak-gatekeeper

For more details refer to the [Documentation](https://www.keycloak.org/docs/latest/securing_apps/index.html#_keycloak_generic_adapter).


## Building from Source

To build from source refer to the [building and working with the code base](docs/building.md) guide.

### Writing Tests

To write tests refer to the [writing tests](docs/tests-development.md) guide.

## Contributing

Before contributing to Gatekeeper please read our [contributing guidelines](CONTRIBUTING.md).


## Other Keycloak Projects

* [Keycloak](https://github.com/keycloak/keycloak) - Keycloak Server and Java adapters
* [Keycloak Documentation](https://github.com/keycloak/keycloak-documentation) - Documentation for Keycloak
* [Keycloak QuickStarts](https://github.com/keycloak/keycloak-quickstarts) - QuickStarts for getting started with Keycloak
* [Keycloak Docker](https://github.com/jboss-dockerfiles/keycloak) - Docker images for Keycloak
* [Keycloak Node.js Connect](https://github.com/keycloak/keycloak-nodejs-connect) - Node.js adapter for Keycloak
* [Keycloak Node.js Admin Client](https://github.com/keycloak/keycloak-nodejs-admin-client) - Node.js library for Keycloak Admin REST API


## License

* [Apache License, Version 2.0](https://www.apache.org/licenses/LICENSE-2.0)
