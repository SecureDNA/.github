# SecureDNA

SecureDNA is a free, non-profit screening platform designed to safeguard DNA synthesis everywhere.

## Availability

- You can find information about the project as a whole, including [papers](https://securedna.org/research) and a [live demo](https://securedna.org/demo/), at the [main site](https://securedna.org).
- Precompiled `synthclient` binaries and certificate tools are available for [Ubuntu amd64 and arm64](https://github.com/SecureDNA/ppa).
- Docker/podman container images are also available:
  - As a minimal-size image containing just `synthclient`: `docker pull ghcr.io/securedna/synthclient`
  - As an image containing both `synthclient` and the tools required to request a certificate and generate authorization tokens: `docker pull ghcr.io/securedna/synthclient-tools`
- Source for the client and servers is available in our [monorepo](https://github.com/SecureDNA/SecureDNA).
  - You can compile this source and run test servers using test databases and your own test certificates.  To screen with a real database, see [below](#performing-screening).
  - [quickdna](https://github.com/SecureDNA/quickdna) is a general-purpose DNA manipulation tool but does not have to be separately downloaded to build or run the servers or client.

## Performing screening

- To use the production servers and hence screen using real databases, you'll need to [obtain certificates](https://securedna.org/start/) by following the [quickstart instructions](https://pages.securedna.org/production/assets/Synthclient-quickstart.pdf).
- For automated use, consult our [API documention](https://pages.securedna.org/production/assets/Synthclient-API.pdf)
- Results can also be visualized at http://localhost:80/; see the [quickstart](https://pages.securedna.org/production/assets/Synthclient-quickstart.pdf) for more information.
