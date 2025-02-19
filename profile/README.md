# SecureDNA

SecureDNA is a free, non-profit DNA synthesis screening platform dedicated to safeguarding the future of biotechnology. Our state-of-the-art, privacy-preserving system is designed to verify the safety of DNA sequences before synthesis—protecting public health, supporting regulatory compliance, and preserving your intellectual property.

- [Why SecureDNA?](#why-securedna)
- [Why It Matters](#why-it-matters)
- [Installation](#installation)
- [Documentation](#documentation)
- [Questions or Assistance](#questions-or-assistance)

## Why SecureDNA?

- **Ultra-Sensitive Screening:** Detects hazardous sequences as short as 30 base pairs (or 20 amino acid peptides) with unparalleled accuracy.
- **Comprehensive Database:** Continuously updated with an exhaustive range of pathogens, emerging threats, and functional variants to stay ahead of biosecurity risks.
- **Advanced Cryptography:** Leverages cutting-edge techniques, including Distributed Oblivious Pseudorandom Function (DOPRF), blinding, and one-way hashing to ensure that your sensitive sequence data remains confidential throughout the screening.
- **Free:** Our lightning-fast service is offered at no charge, lowering the barrier for adoption and supporting safe scientific innovation worldwide.
- **Seamless Integration:** Easily integrate SecureDNA into your existing workflows via a developer-friendly REST API or interact with our intuitive web UI.

## Why It Matters

As DNA synthesis becomes faster and more accessible, ensuring that harmful sequences are not inadvertently produced is crucial. SecureDNA empowers providers to screen synthesis orders effectively—mitigating biosecurity threats, supporting regulatory adaptation, and protecting both scientific progress and public safety.

## Installation

### 1. Obtain Your Certificate

- SecureDNA requires a certificate to authenticate screening requests and prevent abuse. To obtain your access certificate, generate and submit a certificate request file.
- You can generate your certificate request file locally using our [in-browser generation form](https://securedna.org/cert-request/) , or via [CLI](https://github.com/SecureDNA/SecureDNA/wiki/Synthclient-quickstart:-Tokens-via-CLI).
- Once your certificate request file has been generated, please complete a brief [registration form](https://securedna.org/start/) and attach the certificate request file to the bottom of the form before submitting (in-browser certificate request generation should automatically redirect you to the registration form once you have successfully saved the generated files.)

**Getting Started with Your Certificate**

- Once you have submitted your registration form with your certificate request file, our team will review your application. Upon approval, you will be provided with a signed access certificate. This signed certificate allows you to generate [authorization tokens](https://github.com/SecureDNA/SecureDNA/wiki/Synthclient-quickstart:-Tokens-via-browser#generating-synthesizer-tokens), which are essential for accessing our screening servers.

**What You Need to Do:**
- **Keep Your Certificate Secure:** Safeguard your private key (`.priv` file) and passphrase. They are critical for authenticating your _synthclient_.
- **Generate Authorization Tokens:** These tokens are used by _synthclient_ for every screening request.
  - Refer to the sections on [Browser token generation](https://github.com/SecureDNA/SecureDNA/wiki/Synthclient-quickstart:-Tokens-via-browser#generating-synthesizer-tokens) and [CLI token generation](https://github.com/SecureDNA/SecureDNA/wiki/Synthclient-quickstart:-Tokens-via-CLI#using-the-provided-certificate) in our [Quickstart Wiki](https://github.com/SecureDNA/SecureDNA/wiki) for additional detailed instructions on generating screening authorization tokens.

### 2. Choose Your Installation Method

We support multiple installation options to accommodate different systems and preferences:
- **Ubuntu/Debian (APT-based systems):** Refer to [Installing the PPA](https://github.com/SecureDNA/SecureDNA/wiki/Synthclient-quickstart:-Running-synthclient#installing-the-ppa) in the Quickstart Wiki.
- **Red Hat/CentOS (YUM-based systems):** Refer to [Installing the RPM](https://github.com/SecureDNA/SecureDNA/wiki/Synthclient-quickstart:-Running-synthclient#installing-the-rpm) in the Quickstart Wiki.
- **Docker Users:** Refer to [Installing the Container Image](https://github.com/SecureDNA/SecureDNA/wiki/Synthclient-quickstart:-Running-synthclient#installing-the-container-image) in the Quickstart Wiki.

### 3. Run _synthclient_

After installation, you can run _synthclient_ either as:
- **A Standalone Binary:** Instructions are available under [Running as a Standalone Binary.](https://github.com/SecureDNA/SecureDNA/wiki/Synthclient-quickstart:-Running-synthclient#running-as-a-standalone-binary)
- **A Docker Container:** Guidance is provided under [Running as a Container Image.](https://github.com/SecureDNA/SecureDNA/wiki/Synthclient-quickstart:-Running-synthclient#running-as-a-container-image)

### 4. Integrate _synthclient_ into Your Workflow

With _synthclient_ up and running, you can:
- **Automate Screenings:** Use synthclient's REST API to integrate screening into your order-processing workflow. Refer to our [API Documentation](https://github.com/SecureDNA/SecureDNA/wiki/Synthclient-API) for details.
- **Use the Web Interface:** For visualizing results and debugging, _synthclient_ offers a built-in web UI. Instructions are under [Connecting to synthclient](https://github.com/SecureDNA/SecureDNA/wiki/Synthclient-quickstart:-Running-synthclient#using-the-visualizer) in the Quickstart Guide.

## Documentation

**We have various project documentation and resources available including:**
- Our [FAQ](https://securedna.org/faq/)
- [Research papers](https://securedna.org/research)
- [A live demo](https://securedna.org/demo/)
- A [hazards list](https://securedna.org/hazards/)
- Information on our [Foundation Council, Academic Advisors, and Team](https://securedna.org/team/)

**Additional technical resources:**
- Precompiled `synthclient` binaries and certificate tools are available for [Ubuntu amd64 and arm64](https://github.com/SecureDNA/ppa).
- Docker/podman container images are also available:
  - As a minimal-size image containing just `synthclient`: `docker pull ghcr.io/securedna/synthclient`
  - As an image containing both `synthclient` and the tools required to request a certificate and generate authorization tokens: `docker pull ghcr.io/securedna/synthclient-tools`
- Source for the client and servers is available in our [monorepo](https://github.com/SecureDNA/SecureDNA).
  - You can compile this source and run test servers using test databases and your own test certificates.
  - [quickdna](https://github.com/SecureDNA/quickdna) is a general-purpose DNA manipulation tool but does not have to be separately downloaded to build or run the servers or client.
 
## Questions or Assistance

SecureDNA is not just a tool; it’s a commitment to safe, transparent, and responsible DNA synthesis. By using our free screening system, you help protect global health, support regulatory adaptation, and foster innovation in synthetic biology.

For more information, visit [securedna.org](https://securedna.org) or contact us at [onboarding@securedna.org](mailto:onboarding@securedna.org).
