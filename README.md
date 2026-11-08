# Awesome-Account-Subscription-Management

# Awesome-Account-Subscription-Management
**Top Account Subscription Management (Opensource) 🌟 Star if you like it! 🌟**

**Curated List of SaaS Products & Open-Source GitHub Projects**
*Focused on Admin Consoles, User Provisioning, Subscription Lifecycle & Self-Hosted Identity Governance*
**Last updated: November 2026**

This repository tracks notable **SaaS platforms** and **open-source projects** for **Account & Subscription Management**. These tools enable organizations to centralize user administration, manage product subscriptions and licenses, automate onboarding/offboarding, and govern access across their software estate—from fully managed admin consoles within large SaaS suites to open-source identity governance platforms that give teams complete control over provisioning and entitlement data.

**Examples** include Atlassian Admin, Freshworks Admin Center, Zendesk Admin Center, Salesforce Setup, ServiceNow Subscription Management, HubSpot Account Settings, Zoho Directory, Workday Admin, and Intercom Settings (the category leaders in commercial space).

**Open-source emphasis**: This section is expanded with every relevant project for self-hosted identity governance, user provisioning, and subscription billing. **Critical note**: The open-source landscape is anchored by **Apache Syncope**—the Apache-governed identity governance platform with SCIM, SAML, OIDC, and 16 pre-built connectors for LDAP, AD, Azure, Okta, and ServiceNow . **Kill Bill** is the most mature open-source subscription billing engine, in production since 2010 with no per-transaction fees . No open-source project matches Freshworks Admin Center's multi-product billing unification or Zendesk's native provisioning setup, but for core provisioning and subscription logic, the options are production-proven.

Contributions welcome! Open a PR to add/update entries. Keep descriptions factual and link to official sites.

## Table of Contents
- [SaaS/Hosted Platforms](#saas-hosted-platforms)
- [Open-Source GitHub Projects](#open-source-github-projects)
- [How to Contribute](#how-to-contribute)
- [Disclaimer](#disclaimer)

## SaaS/Hosted Platforms

- **Atlassian Admin**
  **Centralized administration** for Atlassian Cloud organizations. **Features**: Domain verification and account claiming; **SCIM provisioning** from Okta and other IdPs; SAML SSO via Atlassian Guard; managed accounts with enforced security policies . **Pricing**: Included with Atlassian subscriptions; Atlassian Guard for advanced security (30-day free trial then billed per managed account). **Free tier**: Limited. **Best for**: Atlassian customers wanting native user lifecycle management across Jira, Confluence, and Bitbucket—**trade-off**: provisioning requires Atlassian Guard and domain verification.

- **Freshworks Admin Center (Neo)**
  **Unified administration** across Freshworks products. **Features**: **Single console for users, security policies, and subscription billing**; SSO via SAML/OAuth2/OIDC/JWT; 2FA enforcement; audit logs; self-serve license purchases; unified organization binding all product accounts . **Pricing**: Included with Freshworks subscriptions. **Free tier**: Limited. **Best for**: organizations running multiple Freshworks products wanting one admin plane—**trade-off**: Freshdesk account admins are not automatically Org Admins; privileges must be granted .

- **Zendesk Admin Center**
  **Administration console** for Zendesk support suite. **Features**: **SCIM provisioning via Microsoft Entra ID** with automatic user create/update/delete; SAML SSO; API token management; role synchronization from IdP to Zendesk . **Pricing**: Included with Zendesk; provisioning requires Professional plan or better. **Free tier**: None for SCIM. **Best for**: Zendesk customers wanting automated user lifecycle from Entra ID—**trade-off**: SCIM requires Professional plan minimum and API token setup .

- **ServiceNow Subscription Management**
  **License and subscription tracking** within ServiceNow platform. **Features**: Subscription usage visibility; role-based license allocation (ITIL, Approver User); **subscription count updates can lag up to 3 days** after role changes . **Pricing**: Included with ServiceNow subscriptions; licenses per fulfiller role. **Free tier**: None. **Best for**: ServiceNow customers needing visibility into fulfiller license consumption—**trade-off**: subscription reflection delay requires patience and role audits; contact Account Executive for contract details .

- **HubSpot Account Settings**
  **Account administration** for HubSpot CRM. **Features**: User invitation and permission management; **SSO for Enterprise only** (including ADFS); 2FA; team management for Professional/Enterprise . **Pricing**: Included with HubSpot tiers; SSO requires Enterprise. **Free tier**: Limited. **Best for**: HubSpot users managing teams and permissions within CRM—**trade-off**: SSO gated to Enterprise; no SCIM provisioning mentioned in available documentation.

- **Zoho Directory**
  **Workforce identity platform** within Zoho ecosystem. **Features**: **SCIM provisioning from Entra ID or Okta**; SAML SSO; group-to-role mapping; AD Sync tool for on-premises Active Directory . **Pricing**: Included with Zoho Workplace/ecosystem. **Free tier**: Limited. **Best for**: Zoho-centric organizations wanting directory and SSO—**trade-off**: SCIM is one-way (Entra → Zoho); no writeback .

- **Workday Admin (UPA)**
  **Unified provisioning and authentication** for Workday Adaptive Planning. **Features**: **UPA streamlines user sync and SSO** for Adaptive Planning; User Provisioning Workspace (UPW) for security groups; Unified Access Management (UAM) for automated permission management across Workday and Adaptive Planning . **Pricing**: Included with Workday. **Free tier**: None. **Best for**: Workday customers implementing Adaptive Planning—**trade-off**: non-production setup requires IMPL tenant (Sandbox resets weekly) .

- **Salesforce Setup**
  **Administration console** for Salesforce. **Pricing**: Included with Salesforce licenses. **Free tier**: Developer edition. **Best for**: Salesforce admins managing users and permissions—**note**: limited public documentation in available search results.

- **Intercom Settings**
  **Administration** for Intercom workspace. **Pricing**: Included with Intercom. **Free tier**: Limited. **Best for**: Intercom users managing teammates and permissions—**note**: limited public documentation in available search results.

## Open-Source GitHub Projects

- **Apache Syncope**
  **Open-source identity management and governance platform** (Apache 2.0) — **the most complete open-source account and subscription lifecycle platform**, maintained by the Apache Software Foundation . **Features**: **Full identity lifecycle**—create, update, provision, reconcile, and deprovision users, groups, and accounts; **approval workflows** for access requests; **password and account policies**; **auditable record** of who has access to what; **REST APIs** for automation; **16 pre-built ConnId connectors** covering LDAP, Active Directory, relational databases, CSV, SCIM, REST, SOAP, Azure, Okta, Google Apps, and ServiceNow . **Supported standards**: SAML 2.0, OpenID Connect, SCIM 2.0 . **Tech stack**: Java, Tomcat, PostgreSQL. **Deploy**: Self-hosted (Docker, VM) or cloudimg-managed image with security hardening (per-instance secrets generated on first boot) . **Trade-off**: **Enterprise-oriented**—requires Java infrastructure and identity governance expertise; commercial support via cloudimg ($0.04/vCPU-hour for packaging and patching) . **Best for**: organizations needing full identity governance with provisioning workflows, audit trails, and multi-system connectors—especially regulated industries with compliance requirements.

- **Kill Bill**
  **Open-source subscription billing and payments platform** (Apache 2.0) — **the most mature open-source subscription management engine**, in production since 2010 and invoicing billions of dollars . **Features**: **Catalog-driven subscriptions**—products, plans, phases, trials, add-ons, and price lists versioned by effective date; **plan changes** immediate or end-of-term with automatic credit/proration; **invoicing and payments** via plugins for Stripe, Braintree (PayPal), Adyen, and others; **tax plugins** for Avalara, Vertex, and Kintsugi; **multi-tenant billing** with separate catalogs per tenant; **usage billing** for AI tokens, API calls, and compute hours; **MRR, churn, and subscription reporting** in Kaui admin UI . **Pricing**: **Free (Apache 2.0, self-hosted, no per-transaction fees)**; **Aviate enterprise at $9,999/month billed annually** adds metering, prepaid credits, coupons, catalog UI, and Level 3 support . **Tech stack**: Java, MySQL/MariaDB/PostgreSQL. **Deploy**: Self-hosted (Docker, on-premises, any cloud) . **Trade-off**: **Billing engine, not a full account admin console**—no user provisioning or SSO; pair with Syncope for identity lifecycle. **Best for**: SaaS and subscription businesses wanting full control over billing logic without per-transaction vendor fees—especially those with complex pricing models (usage tiers, prepaid credits, multi-tenant).

- **FusionDirectory**
  **Modern identity management solution** (open source) — **a complete IAM suite** for managing users, groups, and organizational units . **Features**: Web-based administration; LDAP-backed; role-based access; plugin architecture for extensions (including FusionDirectory Plugins for additional functionality) . **Tech stack**: PHP, LDAP. **Deploy**: Self-hosted. **Trade-off**: **LDAP-centric**—requires OpenLDAP or compatible directory; smaller community than Syncope. **Best for**: organizations with existing LDAP infrastructure wanting a modern web console for identity administration.

- **WrenIDM**
  **Community-developed identity management system** (open source) — **a flexible, scriptable IDM platform** with multiple extension points . **Features**: Flexible data model; JavaScript and Groovy scripting support; multiple extension points; community-maintained fork of ForgeRock OpenIDM . **Tech stack**: Java. **Deploy**: Self-hosted. **Trade-off**: **Community fork**—less enterprise support than commercial alternatives; smaller ecosystem. **Best for**: teams wanting a scriptable, extensible IDM platform with community governance—especially those familiar with ForgeRock lineage.

### Additional Strong Open-Source Options

- **Evolveum MidPoint** — Identity management and governance platform (open source, ~373 stars) . Provisioning, synchronization, RBAC, workflows. **Note**: Comprehensive IGA; steeper learning curve. **Best for**: enterprises needing full IGA with synchronization and reconciliation.
- **SCIM server libraries** — Go packages for building SCIM 2.0 servers (`wyolet/relay/auth/scim`, `imulab/go-scim`) . **Note**: **Building blocks, not a platform**—for developers implementing SCIM provisioning endpoints. **Best for**: teams building custom SCIM targets for IdPs.
- **FusionDirectory Plugins** — Extensions for FusionDirectory (open source) . **Note**: Extends FusionDirectory; not standalone. **Best for**: FusionDirectory users needing additional features.

**Frameworks for building custom systems**: Combine **Apache Syncope** for identity governance and provisioning with **Kill Bill** for subscription billing and **FusionDirectory** for LDAP administration—creating a complete open-source account and subscription management stack. **None of these match Freshworks' multi-product billing unification or Atlassian's managed account claiming**, but for core provisioning, entitlement management, and subscription logic, the options are production-proven.

## How to Contribute

1. Fork the repo.
2. Add/edit entries in `README.md` (follow existing format).
3. Include: name, link, 1–2 sentence description, license (for open-source), and whether it's SaaS or open-source.
4. Submit PR with a short explanation.

Star the repo if you find it useful!

## Disclaimer

- This is a **community-curated** list — not exhaustive and not an endorsement.
- Account and subscription management platforms handling user identities and billing data must comply with data protection regulations (GDPR, CCPA, etc.) and implement appropriate access controls.
- **The "SaaS admin console" vs. "identity governance platform" vs. "subscription billing engine" distinction is critical.** **Atlassian Admin, Freshworks Admin Center, Zendesk Admin Center, HubSpot Account Settings, Zoho Directory, and Workday UPA** are **SaaS admin consoles**—they manage users and subscriptions within their own product suites . **ServiceNow Subscription Management** is **license tracking**—it shows fulfiller consumption but not external billing . **Apache Syncope and FusionDirectory** are **identity governance platforms**—they provision and govern users across systems . **Kill Bill** is a **subscription billing engine**—it creates subscriptions, invoices, and payments, but does not manage user accounts or SSO . **Choose based on whether you need product-native admin, cross-system governance, or billing logic.**
- **Apache Syncope is the most complete open-source account lifecycle platform**—with 16 connectors, approval workflows, and full audit trails . **The trade-off**: enterprise complexity; requires identity governance expertise.
- **Kill Bill is the most mature open-source subscription engine**—in production since 2010 with no per-transaction fees, and a clear path to Aviate enterprise at $9,999/month . **The trade-off**: it is billing, not account administration; pair with Syncope for identity.
- **Zendesk SCIM provisioning requires Professional plan or better** and API token setup in Admin Center . **The trade-off**: Entra ID provisioning is well-documented, but plan tier gates the capability.
- **ServiceNow subscription counts can lag up to 3 days** after role changes . **Do not assume real-time reflection**—audit ITIL roles independently before renewal conversations.
- **Freshworks Admin Center's multi-product billing unification** is a genuine differentiator—one console for users, security, and subscriptions across products . **The trade-off**: Org Admin privileges must be explicitly granted; Freshdesk admins are not auto-promoted .
- Self-hosted open-source solutions require proper infrastructure (Java for Syncope and Kill Bill, PostgreSQL for both), security hardening, and ongoing maintenance. **Account and billing platforms handle sensitive identity and financial data**—ensure your deployment meets your organization's security and compliance requirements before migrating production data.

---

**Made for IT administrators, identity engineers, and organizations building transparent account and subscription management solutions.**
Let's make Account & Subscription Management more open, data-driven, and lifecycle-aware.
