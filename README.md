# Sadeem SaaS Package

> Transform your Odoo instance into a professional SaaS hosting platform — self-hosted.

![Odoo Version](https://img.shields.io/badge/Odoo-18%2B-purple)
![Version](https://img.shields.io/badge/version-18.0.1.0.0-green)

---

## ⚠️ Disclaimer — Read Before Use

We trust you have received the usual lecture from your system administrator.
It usually boils down to these three things:

```
#1) Test in a non-production environment first.
#2) Read the documentation before clicking buttons.
#3) Take backups before changing anything.
```

This software is provided "as is", without warranty of any kind, express or
implied, including but not limited to the warranties of merchantability,
fitness for a particular purpose and noninfringement. In no event shall the
authors or copyright holders be liable for any claim, damages, or other
liability, whether in an action of contract, tort, or otherwise, arising
from, out of, or in connection with the software or the use or other
dealings in the software.

By installing this module, you accept full responsibility for any consequences
of its operation, including but not limited to data loss, service downtime,
billing errors, security incidents, or unexpected charges from third-party
providers (Cloudflare, AWS, hosting providers, etc.).

You are solely responsible for:

- Securing the credentials you configure (API keys, SSH keys, passwords)
- Maintaining backups of your data
- Reviewing and understanding what each automated action does
- Complying with the laws of your jurisdiction
- Monitoring your infrastructure costs

If you are not comfortable with the above, please stop here and contact
support@sadeem.cloud to discuss managed hosting instead.

See [DISCLAIMER.md](DISCLAIMER.md) for the full disclaimer.

---

## What is Sadeem SaaS Package?

Sadeem SaaS Package is an Odoo module that turns a single Odoo instance into a complete SaaS
hosting management platform. It automates the entire client-onboarding pipeline — DNS, SSL,
container deployment, module installation, and backups — so a new customer can be provisioned
in under 5 minutes from a confirmed invoice.

The platform is used in production by Odoo Partners managing 80+ client subscriptions from a
single Odoo dashboard.

---

## Commercial Services

The Sadeem team supports the platform through:

- **Managed hosting** — we run the infrastructure for you
- **Custom development** — features built to your specification
- **Paid technical support** — billable hours for installation, configuration, and troubleshooting

> **Note:** There is no free community support. Issues opened on GitHub are reviewed when time
> permits but carry no SLA. For guaranteed response times, contact support@sadeem.cloud about
> paid support.

---

## Documentation

Full documentation is at: **https://saas.docs.sadeem.cloud**

It covers:

- Architecture overview and the three deployment planes
- Getting started — prerequisites, installation, first subscription
- Docker vs DBFilter decision guide
- Tutorials (Cloudflare, backups, trial flow, customer portal, migration from Odoo.sh)
- Troubleshooting (build failures, SSH issues, DNS, backups, notifications)
- Developer reference for all 15 modules
- API reference (webhooks, integrations)

---

## Repository Structure

```
SAASPackagePublic/
├── LICENSE                    # License
├── README.md                  # This file
├── DISCLAIMER.md              # Extended disclaimer
└── saas_package/              # Master module
    ├── __manifest__.py
    ├── __init__.py
    └── ...
```

> **Important:** Place the `saas_package` folder (or a parent directory containing it) on your
> Odoo addons path, then install **Sadeem SaaS Package** from Apps. Sub-modules will install
> automatically.

---

## Installation

### Prerequisites

- Odoo 18 or newer
- A running PostgreSQL server
- (Optional but recommended) A Cloudflare account, a Portainer instance, an Nginx Proxy Manager
  instance — see the documentation for full prerequisites.

### Quick Install

```bash
# Clone the repo into your Odoo addons directory
cd /path/to/your/odoo/addons
git clone https://github.com/sadeem-cloud-org/saas-package-public.git

# Or download a release tarball
wget https://github.com/sadeem-cloud-org/saas-package-public/archive/refs/heads/main.tar.gz
tar -xzf main.tar.gz

# Restart Odoo with the addons path including the cloned folder
# Then activate developer mode and install "Sadeem SaaS Package" from Apps
```

For step-by-step setup including all integrations, see the
[Getting Started guide](https://saas.docs.sadeem.cloud/user-guide/getting-started/).

### Supported Odoo Versions

The master module runs on Odoo 18+. Customer subscriptions managed by Sadeem can run any version
from Odoo 14 through 19.

---

## Contributing

Issues and pull requests are welcome via GitHub. Please:

- Open an issue first to discuss significant changes before submitting a PR
- Follow Odoo coding conventions
- Test your changes against a real Odoo 18 instance before submitting

Bug reports without reproduction steps will likely be closed.

---

## Commercial Services

For paid services around the platform, contact us:

| Service | Channel |
|---|---|
| Managed hosting | support@sadeem.cloud |
| Custom development | support@sadeem.cloud |
| Paid technical support | support@sadeem.cloud |
| General inquiries | https://sadeem.cloud |
| WhatsApp | +20 114 353 5115 |

---

## About Sadeem

Sadeem is an Egyptian/Saudi technology company specializing in Odoo development, SaaS solutions,
and cloud infrastructure. Founded in 2020 as Digital X, rebranded to Sadeem in 2023.

Website: https://sadeem.cloud

---

*© 2026 Sadeem.*
