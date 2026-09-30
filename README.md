# Awesome-Certificate-Lifecycle-Management

# Top Certificate Lifecycle Management Platforms Ecosystem

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on CLM, PKI, Automated Certificate Issuance & Expiry Monitoring*
**Last updated: September 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Certificate Lifecycle Management (CLM)**. These tools help organizations discover, issue, renew, revoke, and monitor X.509 and SSH certificates across hybrid and multi-cloud environments—preventing outages from expired certificates and enforcing cryptographic policy.

**Examples** include Keyfactor, Venafi, DigiCert Trust Lifecycle Manager, Sectigo Certificate Manager, Entrust Certificate Hub, AppViewX, KeyTalk, ManageEngine Key Manager Plus, GlobalSign Atlas, Fortanix, and Smallstep (the category leaders).

**Open-source emphasis**: Certificate lifecycle management has a **mature and production-proven open-source ecosystem**. **EJBCA** (sponsored by Keyfactor) is one of the world's most popular open-source PKIs, with over two decades of development and Common Criteria certification . **step-ca** (Smallstep) provides a modern, developer-friendly online CA with ACME and OIDC support . **Dogtag PKI** is the certificate system underlying Red Hat's identity management . **CFSSL** (CloudFlare) offers a PKI/TLS toolkit for signing, verifying, and bundling certificates . **Certify The Web** provides a professional ACME client for Windows used by 150,000+ organizations . This section documents these production-grade solutions.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents

- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **[Keyfactor](https://www.keyfactor.com/)**
  Enterprise PKI and CLM platform. The open-source **EJBCA** is sponsored by Keyfactor, providing a bridge between community and enterprise PKI .

- **[Venafi](https://venafi.com/)**
  Machine identity management platform. Provides **TLS Protect** for certificate lifecycle automation and a **Vault PKI Secrets Engine plugin** for HashiCorp Vault integration .

- **[DigiCert Trust Lifecycle Manager](https://www.digicert.com/)**
  Certificate lifecycle management platform. Provides discovery, issuance, renewal, and revocation across public and private CAs.

- **[Sectigo Certificate Manager](https://sectigo.com/)**
  CLM platform for discovering, issuing, and managing certificates. Provides automation and policy enforcement.

- **[Entrust Certificate Hub](https://www.entrust.com/)**
  Certificate lifecycle management platform. Provides discovery, automation, and compliance for enterprise PKI.

- **[AppViewX](https://www.appviewx.com/)**
  CLM and automation platform. Provides certificate discovery, issuance, renewal, and policy enforcement across multi-cloud.

- **[KeyTalk](https://www.keytalk.com/)**
  CLM platform with certificate automation and identity management capabilities.

- **[ManageEngine Key Manager Plus](https://www.manageengine.com/)**
  Certificate lifecycle management. Provides discovery, tracking, renewal, and compliance reporting.

- **[GlobalSign Atlas](https://www.globalsign.com/)**
  Cloud-based certificate management platform. Provides automated issuance, renewal, and policy enforcement.

- **[Fortanix](https://www.fortanix.com/)**
  Data security platform with certificate lifecycle management and HSM-backed key protection.

## Open-Source GitHub Projects

### Full PKI & Certificate Authority Platforms

- **[EJBCA](https://github.com/Keyfactor/ejbca-ce)**
  **The most mature and widely deployed open-source PKI and Certificate Authority.** **LGPL v2.1 licensed**, sponsored by Keyfactor . **One installation supports multiple secure, separated, and independent PKIs** simultaneously using a modular architecture for CA, Registration Authority (RA), and Validation Authority (OCSP/CRL) . **Supports a wide variety of enrollment protocols, integration interfaces, certificate profiles, and cryptographic algorithms** . Platform-independent, can be scaled out and in to match needs. **Deployment**: Docker containers, Helm charts, and Ansible playbooks for automation . **Common Criteria certified** since 2008 . Enterprise edition available with SLAs, security configurations, and additional deployment options (appliance, cloud, SaaS) .

- **[step-ca (Smallstep)](https://github.com/smallstep/certificates)**
  **The leading modern open-source online Certificate Authority for DevOps.** **Apache-2.0 licensed**, maintained by Smallstep Labs . **Features**: X.509 and SSH certificate issuance; **ACME v2 server** supporting all popular challenge types; **OIDC provisioners** for Okta, GSuite, Azure AD, Auth0, Keycloak, Dex ; **Cloud instance identity document provisioners** for AWS, GCP, Azure VMs ; **Single-use JWK tokens** for CD tool integration (Puppet, Chef, Ansible, Terraform) ; **X5C provisioner** for trusted X.509 certificates . **Key types**: RSA, ECDSA, EdDSA . **Backends**: Badger, BoltDB, PostgreSQL, MySQL . **Short-lived certificates** with automated enrollment, renewal, and **passive revocation** . **Limitations**: Single Intermediate CA, offline root CA, authority-wide policies, limited active revocation (CRL/OCSP), no Certificate Transparency integration, no ACME EAB .

### PKI Toolkits & Certificate Authority Frameworks

- **[CFSSL (CloudFlare)](https://github.com/cloudflare/cfssl)**
  **CloudFlare's PKI/TLS Swiss Army knife.** **MIT licensed** . **Both a command-line tool and an HTTP API server** for signing, verifying, and bundling TLS certificates . **Components**: `cfssl` (command line utility), `multirootca` (certificate authority server with multiple signing keys), `mkbundle` (certificate pool bundle builder), `cfssljson` (JSON output to certificate/key/CSR/bundle files) . Requires Go 1.16+ to build .

- **[Dogtag PKI](https://github.com/dogtagpki/pki)**
  **The Certificate System PKI suite underlying Red Hat's identity management.** **Dogtag PKI Suite** includes Certificate Authority (pki-ca), Data Recovery Manager (pki-kra), Online Certificate Status Protocol Manager (pki-ocsp), Token Key Service (pki-tks), and Token Processing System (pki-tps) . Available in Ubuntu and Debian repositories .

### Certificate Lifecycle & Discovery Tools

- **[Certify The Web](https://github.com/webprofusion/certify)**
  **Professional ACME Client for Windows with Certificate Management UI.** **Used by over 150,000 organizations** . Powered by Let's Encrypt and **compatible with all ACME v2 CAs** . **C# based**, 1,600+ stars, 277 forks, actively maintained (updated daily) . Provides certificate management, deployment tasks, and chain checking .

- **[CertHound Agent](https://github.com/deadbolthq/certhound-agent)**
  **Cross-platform SSL/TLS certificate inventory and managed-renewal agent.** **Single-binary Go agent** with no runtime dependencies . **Filesystem scanning** for PEM/CRT/DER certificates and **Windows certificate store** enumeration . **ACME managed-renewal** via Let's Encrypt with HTTP-01 webroot challenge . **Fleet-wide visibility** with centralized dashboard reporting, expiry alerts, and auto-update . **Watch mode** with daily full scans and fsnotify-triggered scans .

- **[CertMate](https://github.com/fabriziosalmi/certmate)**
  **Certificate lifecycle management with discovery and inventory.** **v2.24.0** adds **TLS probe** for inspecting certificates served at host:port, **fingerprint-keyed inventory** in SQLite, **scheduled endpoint discovery**, **CT-log monitoring** via crt.sh for shadow-issuance detection . **Adopt discovered certificates** into normal renewal schedules . **Cryptographic readiness report** classifying algorithms as weak/acceptable/modern with quantum-vulnerability flags .

- **[pki-manager-web](https://github.com/oriolrius/pki-manager-web)**
  **Self-hosted web PKI for the full X.509 and SSH certificate lifecycle.** **Private keys in Cosmian KMS** . **Features**: Revocation tracking with detailed reasons, secure key pair generation (RSA, ECDSA), OIDC authentication (Keycloak, Auth0, Okta, Azure AD), role-based access control . **Dual User + Host OpenSSH CA** with per-host access blocks, two-tier KRL revocation, and `krl-client` host agent . **Kubernetes cert-manager external issuer** API . **Tech stack**: Node.js/Fastify backend, React 19 frontend, SQLite, tRPC API .

### Kubernetes-Native Certificate Management

- **[cert-manager](https://github.com/cert-manager/cert-manager)**
  **The de facto standard for automated TLS certificate management in Kubernetes.** **Microsoft-supported distribution available via Azure Arc** (preview) with enterprise support, proactive updates, and security patches . **Features**: Automated certificate lifecycle (issuance, renewal before expiry); **trust-manager** for central CA bundle distribution across namespaces; integration with **self-signed CAs or external enterprise PKI** (ACME providers, corporate CAs); **offline and edge-friendly** operation . **Validated on AKS, EKS, GKE, and Arc-enabled Kubernetes distributions** .

### Additional Strong Open-Source Options

- **Full PKI/CA**: **EJBCA** (most mature, LGPL, Common Criteria, Keyfactor-sponsored) , **step-ca** (modern DevOps, ACME, OIDC) .
- **PKI Toolkits**: **CFSSL** (CloudFlare, MIT, CLI + API) , **Dogtag PKI** (Red Hat-backed, full suite) .
- **CLM & Discovery**: **Certify The Web** (Windows, 150k+ orgs) , **CertHound** (cross-platform agent, fleet visibility) , **CertMate** (discovery + inventory + readiness) .
- **SSH CA**: **pki-manager-web** (dual X.509 + SSH CA, Kubernetes external issuer) , **step-ca** (SSH certificates for people and hosts) .
- **Kubernetes**: **cert-manager** (de facto standard, Azure Arc supported) .

**Frameworks for building custom systems**: Combine **EJBCA** for enterprise-grade PKI with multiple CAs and Common Criteria certification, **step-ca** for modern DevOps certificate automation with ACME and OIDC, **cert-manager** for Kubernetes-native certificate lifecycle management, and **CertHound** or **CertMate** for fleet-wide discovery and expiry monitoring. Add **HashiCorp Vault** with the **EJBCA Vault PKI Engine** or **Venafi Vault plugin** for secrets management integration .

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Certificate lifecycle management platforms handle sensitive cryptographic material and private keys; ensure proper HSM/KMS integration, access controls, and compliance with organizational security policies.
- **Open-source reality**: The open-source ecosystem for CLM is **mature and production-proven**. **EJBCA** provides enterprise-grade PKI with Common Criteria certification and multi-CA support, sponsored by Keyfactor . **step-ca** delivers modern DevOps certificate automation with ACME, OIDC, and cloud identity provisioners . **cert-manager** is the de facto Kubernetes standard . **Certify The Web** serves 150,000+ organizations for Windows ACME automation . However, **commercial platforms** (Venafi, Keyfactor Enterprise, DigiCert, AppViewX) provide **discovery at scale, automated policy enforcement, hardware attestation, and enterprise SLAs** that open-source alternatives require significant assembly and operational investment to match. The open-source path is **genuinely viable** for organizations with strong PKI engineering capacity, particularly for internal PKI, DevOps certificate automation, and Kubernetes workloads.

---

**Made for PKI engineers, security architects, DevOps teams, and machine identity specialists.**
Let's make certificate lifecycle management more open, automated, and secure.
