# Awesome Account & Subscription Management

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![Track Updates](https://img.shields.io/badge/updates-active-brightgreen.svg)](https://github.com/ishandutta2007/Awesome-Account-Subscription-Management)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0_1.0-lightgrey.svg)](http://creativecommons.org/publicdomain/zero/1.0/)

> A curated list of enterprise SaaS platforms and open-source GitHub projects for account administration, subscription lifecycle billing, user provisioning (SCIM), license governance, and self-hosted identity governance and administration (IGA).

Star if you find this useful! Contributions are welcome.

---

## Table of Contents

- [Sector Overview & Market Dynamics](#sector-overview--market-dynamics)
- [SaaS & Hosted Admin Platforms](#saas--hosted-admin-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [Architecture & Integration Patterns](#architecture--integration-patterns)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

---

## Sector Overview & Market Dynamics

The convergence of SaaS Management Platforms (SMP) and Identity Governance and Administration (IGA) forms a rapidly expanding enterprise software segment valued at **over $12.5 billion** (SaaS Management Platforms at ~$4.2B with a 15.2% CAGR; Identity Governance & Administration at ~$8.5B–$9.6B with a 14% CAGR, scaling toward $30B+ by the early 2030s). 

The market exhibits **divergent competitive fragmentation**: SaaS Management and subscription billing remain **highly fragmented** across pure-play spend-optimization tools, developer billing engines, and product-specific admin consoles due to decentralized Shadow IT purchasing across departments. Conversely, core Identity Governance and enterprise admin infrastructure are **moderately concentrated** around mega-cap platform vendors (Salesforce, ServiceNow, Workday, Microsoft) and dedicated IAM leaders (SailPoint, Saviynt, Okta), driving widespread consolidation as organizations replace siloed consoles with unified provisioning fabrics.

---

## SaaS & Hosted Admin Platforms

The table below benchmarks category-leading commercial SaaS platforms providing centralized admin suites, automated SCIM provisioning, workforce directory synchronization, and subscription lifecycle controls.

*Sorted in descending order by company scale (Annual Revenue & Valuation).*

| Platform | Company Scale (Revenue / Valuation) | Key Admin & Lifecycle Capabilities | Starting Tier Pricing | Free Tier / Free Trial Limits |
| :--- | :--- | :--- | :--- | :--- |
| **[Salesforce Setup](https://www.salesforce.com/)** | **~$41.5B revenue** / ~$185B–$200B market cap | Enterprise administration console for multi-org setups, user entitlement allocation, role hierarchies, granular permission sets, session policies, and connected app OAuth tokens. | From **$25/user/month** (Starter Suite, billed annually) | **30-day free trial** (Starter Suite) or **14-day free trial** (Service Cloud) with full feature access; free Developer Edition available permanently for testing. |
| **[ServiceNow Subscription Management](https://www.servicenow.com/)** | **~$13.3B revenue** / ~$110B–$115B market cap | Centralized ITAM/ITSM license and subscription tracking. Delivers role-based license allocation (ITIL Fulfillers, Business Stakeholders, Approvers) and compliance auditing against contract caps. *(Note: Allocation updates can lag up to 72 hours).* | Custom enterprise contract (ITSM Fulfiller licenses typically start around **$70–$100/user/month**) | **No standard public free trial**; permanent free developer sandbox instances provided via ServiceNow Developer Program (sleeps after inactivity). |
| **[Workday Admin & UPA](https://www.workday.com/)** | **~$9.55B revenue** / ~$47B–$50B market cap | Unified Provisioning & Authentication (UPA) and User Provisioning Workspace (UPW). Coordinates security groups, automated cross-tenant synchronization, and Adaptive Planning provisioning. | Custom enterprise quotes (Adaptive Planning starts at **~$25,000–$36,000/year** base pilot package) | **30-day free trial** available specifically for Workday Adaptive Planning; enterprise core HCM/Financials requires assisted pilot environment. |
| **[Atlassian Admin & Guard](https://www.atlassian.com/)** | **~$5.22B revenue** / ~$41B–$48B market cap | Centralized organization manager across Jira, Confluence, and Bitbucket. Supports domain verification, account claiming, centralized SAML SSO, and automated SCIM provisioning via Atlassian Guard. | From **$4.35/user/month** (Atlassian Guard Standard for SCIM & SSO; Jira/Confluence paid tiers start at **$7.75/user/month**) | **30-day free trial** of Atlassian Guard Standard/Premium with unlimited user provisioning testing; Jira/Confluence offer a forever-free plan limited to **up to 10 users**. |
| **[HubSpot Account Settings](https://www.hubspot.com/)** | **~$3.13B revenue** / ~$25B–$30B market cap | CRM administrative console governing multi-team partitioning, seat assignment (Core, Sales, Service), role-based permission sets, 2FA enforcement, and SCIM/SAML SSO (Enterprise). | From **$15/seat/month** (Starter Customer Platform); SAML SSO requires Enterprise tiers starting at **$150/seat/month** or **$3,600/month** (Marketing Hub Enterprise) | **Forever-free plan** limited to basic CRM tools and up to **5 users** (with HubSpot branding); **14-day free trial** of Professional and Enterprise suites. |
| **[Zendesk Admin Center](https://www.zendesk.com/)** | **~$2.0B ARR** / ~$10.2B valuation (Private equity) | Centralized customer support administration featuring SCIM automated user lifecycle sync via Microsoft Entra ID and Okta, API token scoping, custom agent roles, and audit trail logs. | From **$19/agent/month** (Support Team); automated SCIM user provisioning requires Suite Professional starting at **$115/agent/month** (billed annually) | **14-day free trial** with full Suite Professional features enabled (including SCIM endpoints and test agent seats). |
| **[Zoho Directory](https://www.zoho.com/directory/)** | **~$1.5B revenue** / ~$12.4B secondary valuation (Bootstrapped) | Complete workforce identity and directory governance platform. Delivers SCIM provisioning from Entra ID/Okta, SAML 2.0 SSO, on-premises Active Directory sync tool, and Cloud RADIUS/LDAP. | From **$1.70/user/month** (Standard plan billed annually) or **$5.95/user/month** (Professional plan) | **Forever-free plan** supporting up to **10 users**, **3 third-party SSO apps**, **2 directory stores**, and 7 days of audit log retention. |
| **[Freshworks Admin Center (Neo)](https://www.freshworks.com/)** | **~$840M–$850M revenue** / ~$3.3B–$3.5B market cap | Unified multi-product admin suite (Neo Platform) spanning Freshdesk, Freshservice, and Freshsales. Centralizes organization-wide identity policies, SAML/OIDC SSO, and multi-product subscription billing into one pane. | From **$19/agent/month** (Freshdesk Growth billed annually); Freshservice starts at **$19/agent/month** | **14-day free trial** with unrestricted enterprise features; optional downgrade to Free Program limited to **up to 2 agents** (basic ticketing and knowledge base for up to 6 months). |
| **[Intercom Workspace Settings](https://www.intercom.com/)** | **~$400M ARR** / ~$3.6B acquisition valuation | Workspace administration for customer communications. Governs teammate seat assignments, permission profiles, automated conversation assignment rules, and security controls. | From **$19/seat/month** (Essential plan billed annually) | **14-day free trial** covering full platform features and Fin AI Agent credit testing. |

---

## Open-Source GitHub Projects

Self-hosted identity governance, automated provisioning, authentication portals, and open-source subscription billing engines.

*Sorted in descending order by GitHub Star count.*

1. **[Keycloak](https://github.com/keycloak/keycloak)** [![GitHub stars](https://img.shields.io/github/stars/keycloak/keycloak?style=social&color=white)](https://github.com/keycloak/keycloak/stargazers)
   - **Focus**: Enterprise Identity and Access Management (IAM)
   - **License**: Apache-2.0 | **Stack**: Java, Quarkus, PostgreSQL / MySQL / CockroachDB
   - **Key Capabilities**: Industry-standard identity and access management providing OpenID Connect, OAuth 2.0, and SAML 2.0 broker services, user federation (LDAP, Active Directory), fine-grained authorization policies, identity brokering, and social login integration.

2. **[Authelia](https://github.com/authelia/authelia)** [![GitHub stars](https://img.shields.io/github/stars/authelia/authelia?style=social&color=white)](https://github.com/authelia/authelia/stargazers)
   - **Focus**: Single Sign-On & Two-Factor Authentication Portal
   - **License**: Apache-2.0 | **Stack**: Go, React, SQLite / PostgreSQL / MariaDB
   - **Key Capabilities**: Cloud-native authentication server providing multi-factor authentication (FIDO2 WebAuthn, TOTP, Duo) and SSO for reverse proxies (Traefik, NGINX, Caddy, Envoy) with OpenID Connect certification and post-quantum cryptography readiness.

3. **[Zitadel](https://github.com/zitadel/zitadel)** [![GitHub stars](https://img.shields.io/github/stars/zitadel/zitadel?style=social&color=white)](https://github.com/zitadel/zitadel/stargazers)
   - **Focus**: Multi-Tenant Identity Infrastructure & B2B IAM
   - **License**: Apache-2.0 | **Stack**: Go, CockroachDB / PostgreSQL
   - **Key Capabilities**: Turnkey B2B identity infrastructure built for SaaS architectures. Delivers native multi-tenancy, self-service organization management, delegated administration, audit logging, Passkeys/FIDO2, and OpenID Connect / SAML / OAuth support.

4. **[SuperTokens Core](https://github.com/supertokens/supertokens-core)** [![GitHub stars](https://img.shields.io/github/stars/supertokens/supertokens-core?style=social&color=white)](https://github.com/supertokens/supertokens-core/stargazers)
   - **Focus**: Modular User Authentication & Session Governance
   - **License**: Apache-2.0 | **Stack**: Java, PostgreSQL / MySQL
   - **Key Capabilities**: Modular open-source alternative to Auth0/Firebase Auth. Provides resilient session management, automated token refresh rotation, passwordless login, social SSO, multi-factor authentication, and multi-tenant organizational isolation.

5. **[Casdoor](https://github.com/casdoor/casdoor)** [![GitHub stars](https://img.shields.io/github/stars/casdoor/casdoor?style=social&color=white)](https://github.com/casdoor/casdoor/stargazers)
   - **Focus**: Agentic & Multi-Protocol IAM Platform with SCIM
   - **License**: Apache-2.0 | **Stack**: Go, React, MySQL / PostgreSQL / SQL Server
   - **Key Capabilities**: Web UI-centric IAM supporting OAuth 2.0, OIDC, SAML, CAS, LDAP, and **SCIM 2.0 user synchronization**. Features built-in enterprise connectors (Google Workspace, Azure AD, Okta), WebAuthn/MFA, and an agent gateway.

6. **[Ory Kratos](https://github.com/ory/kratos)** [![GitHub stars](https://img.shields.io/github/stars/ory/kratos?style=social&color=white)](https://github.com/ory/kratos/stargazers)
   - **Focus**: Headless Cloud-Native Identity & Account Lifecycle Management
   - **License**: Apache-2.0 | **Stack**: Go, PostgreSQL / CockroachDB / SQLite
   - **Key Capabilities**: Headless user management engine handling registration, multi-tenant profile management, passwordless flows, WebAuthn, TOTP MFA, self-service account recovery, and webhook-driven account lifecycle hooks.

7. **[Kill Bill](https://github.com/killbill/killbill)** [![GitHub stars](https://img.shields.io/github/stars/killbill/killbill?style=social&color=white)](https://github.com/killbill/killbill/stargazers)
   - **Focus**: Enterprise Subscription Billing & Payment Engine
   - **License**: Apache-2.0 | **Stack**: Java, MySQL / MariaDB / PostgreSQL
   - **Key Capabilities**: Production-grade subscription management and recurring billing engine operating since 2010. Delivers multi-tenant product catalogs, proration/upgrades, usage/metered billing, invoicing workflows, payment gateway plugins (Stripe, Adyen, Braintree), and tax integration with zero transaction fees.

8. **[Evolveum MidPoint](https://github.com/Evolveum/midpoint)** [![GitHub stars](https://img.shields.io/github/stars/Evolveum/midpoint?style=social&color=white)](https://github.com/Evolveum/midpoint/stargazers)
   - **Focus**: Comprehensive Identity Governance & Administration (IGA)
   - **License**: EUPL-1.2 | **Stack**: Java, PostgreSQL
   - **Key Capabilities**: Full-featured enterprise IGA platform providing automated user provisioning, identity synchronization, entitlement management, role-based access control (RBAC), access certification campaigns, and comprehensive audit compliance reporting.

9. **[Apache Syncope](https://github.com/apache/syncope)** [![GitHub stars](https://img.shields.io/github/stars/apache/syncope?style=social&color=white)](https://github.com/apache/syncope/stargazers)
   - **Focus**: Open-Source Digital Identity & Provisioning Engine
   - **License**: Apache-2.0 | **Stack**: Java, Tomcat, PostgreSQL / MySQL / Oracle
   - **Key Capabilities**: Top-level ASF project delivering full identity lifecycle management (joiner, mover, leaver), access request approval workflows, password policies, and 16+ ConnId connectors (Active Directory, LDAP, SCIM, Azure, ServiceNow, Okta).

10. **[FusionDirectory](https://github.com/fusiondirectory/fusiondirectory)** [![GitHub stars](https://img.shields.io/github/stars/fusiondirectory/fusiondirectory?style=social&color=white)](https://github.com/fusiondirectory/fusiondirectory/stargazers)
    - **Focus**: Web-Based LDAP Identity & Service Directory Management
    - **License**: GPL-2.0+ | **Stack**: PHP, OpenLDAP
    - **Key Capabilities**: Web application designed to manage directory services and corporate accounts within OpenLDAP. Provides unified administration of users, groups, mail accounts, DNS/DHCP configurations, and desktop service entitlements.

11. **[Wren:IDM](https://github.com/WrenSecurity/wrenidm)** [![GitHub stars](https://img.shields.io/github/stars/WrenSecurity/wrenidm?style=social&color=white)](https://github.com/WrenSecurity/wrenidm/stargazers)
    - **Focus**: Scriptable Identity Management & Provisioning Framework
    - **License**: CDDL-1.0 | **Stack**: Java, Groovy / JavaScript
    - **Key Capabilities**: Community-driven fork of OpenIDM providing a flexible data model, scriptable identity synchronization rules (JavaScript/Groovy), connector framework integration, and event-triggered provisioning workflows.

---

## Architecture & Integration Patterns

Understanding the structural separation across layers is essential when assembling an enterprise account and billing architecture:

```
+-----------------------------------------------------------------------+
|                         SaaS Admin Consoles                           |
|       (Atlassian Guard, Zendesk Admin, Salesforce Setup, Zoho)        |
|  - In-product user seats, security settings, role permissions, tokens |
+-----------------------------------+-----------------------------------+
                                    |
            SCIM 2.0 / SAML 2.0 / OIDC Sync Protocols
                                    |
+-----------------------------------v-----------------------------------+
|               Identity Governance & Administration (IGA)              |
|        (Apache Syncope, Evolveum MidPoint, Keycloak, Zitadel)         |
|  - Joiner-Mover-Leaver (JML) lifecycle workflows                      |
|  - Central directory federation (LDAP / Entra ID / Okta)              |
|  - Access certification, entitlement mapping, and audit logging       |
+-----------------------------------+-----------------------------------+
                                    |
                      Webhooks & Account Events
                                    |
+-----------------------------------v-----------------------------------+
|                  Subscription Billing & Metering                      |
|                           (Kill Bill)                                 |
|  - Multi-tenant catalogs, recurring invoices, and payment gateways    |
|  - Consumption-based usage rating (API calls, AI tokens, compute)     |
|  - Prorated tier upgrades, downgrades, and dunning workflows          |
+-----------------------------------------------------------------------+
```

---

## How to Contribute

We welcome additions, corrections, and improvements from the community!

1. Fork the repository.
2. Create a new branch (`git checkout -b add-resource-name`).
3. Add the project or platform following the existing table or list format (ensure descriptions are objective and include verifiable metrics, stack, and pricing data).
4. Run markdown linters if applicable.
5. Submit a descriptive Pull Request.

---

## Disclaimer

- This curated compilation is for informational and educational purposes; inclusion does not constitute commercial endorsement.
- All pricing numbers, seat limits, and company valuations reflect public filings and market data as of late 2024 / 2025 / 2026 and are subject to change by respective vendors.
- Deploying self-hosted account and billing infrastructure requires rigorous security audits, compliance checks (SOC 2, ISO 27001, GDPR, HIPAA, PCI-DSS), and database encryption to safeguard sensitive customer PII and transaction records.
