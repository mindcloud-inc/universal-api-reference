# <img src="https://images.mindcloud.co/apps/icons/mittwald-icon_1775760520202.png" alt="mittwald logo" width="28" height="28"> mittwald: Universal API

Official API wrapper for mittwald hosting, project, infrastructure, and account resources.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mittwaldAPI/latest
- **Category:** IT Operations / DevOps
- **Actions:** 102
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mittwald.de
- **Vendor API docs:** https://api.mittwald.de/v2/openapi.json

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mittwaldAPI/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (102)

### Ai Hosting

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer AI Hosting](actions/get-customer-ai-hosting.md) | GET | Retrieves customer AI hosting details from mittwald API. |
| [Get Project AI Hosting](actions/get-project-ai-hosting.md) | GET | Retrieves project AI hosting details from mittwald API. |

### Ai Hosting Model

| Action | Method | Description |
| --- | --- | --- |
| [List Customer AI Hosting Models](actions/list-customer-ai-hosting-models.md) | GET | Retrieves customer AI hosting models from mittwald API. |
| [List Project AI Hosting Models](actions/list-project-ai-hosting-models.md) | GET | Retrieves project AI hosting models from mittwald API. |

### API Keys

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer AI Hosting Key](actions/get-customer-ai-hosting-key.md) | GET | Retrieves a customer AI hosting key from mittwald API. |
| [Get Project AI Hosting Key](actions/get-project-ai-hosting-key.md) | GET | Retrieves a project AI hosting key from mittwald API. |
| [List Customer AI Hosting Keys](actions/list-customer-ai-hosting-keys.md) | GET | Retrieves customer AI hosting keys from mittwald API. |
| [List Project AI Hosting Keys](actions/list-project-ai-hosting-keys.md) | GET | Retrieves project AI hosting keys from mittwald API. |

### App Installation

| Action | Method | Description |
| --- | --- | --- |
| [List Project App Installations](actions/list-project-app-installations.md) | GET | Retrieves project app installations from mittwald API. |

### App Version

| Action | Method | Description |
| --- | --- | --- |
| [Get App Version](actions/get-app-version.md) | GET | Retrieves app version from mittwald API. |
| [List App Version Update Candidates](actions/list-app-version-update-candidates.md) | GET | Retrieves app version update candidates from mittwald API. |
| [List App Versions](actions/list-app-versions.md) | GET | Retrieves app versions from mittwald API. |

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Get App](actions/get-app.md) | GET | Retrieves app from mittwald API. |
| [List Apps](actions/list-apps.md) | GET | Retrieves apps from mittwald API. |

### Article

| Action | Method | Description |
| --- | --- | --- |
| [Get Article](actions/get-article.md) | GET | Retrieves article from mittwald API. |
| [List Articles](actions/list-articles.md) | GET | Retrieves articles from mittwald API. |

### Backup

| Action | Method | Description |
| --- | --- | --- |
| [List Project Backups](actions/list-project-backups.md) | GET | Retrieves project backups from mittwald API. |

### Backup Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Project Backup Schedules](actions/list-project-backup-schedules.md) | GET | Retrieves project backup schedules from mittwald API. |

### Contracts

| Action | Method | Description |
| --- | --- | --- |
| [Get Mail Address Contract](actions/get-mail-address-contract.md) | GET | Retrieves a mail address contract from mittwald API. |
| [Get Project Contract](actions/get-project-contract.md) | GET | Retrieves a project's contract from mittwald API. |
| [Get Server Contract](actions/get-server-contract.md) | GET | Retrieves a server contract from mittwald API. |
| [List Customer Contracts](actions/list-customer-contracts.md) | GET | Retrieves customer contracts from mittwald API. |

### Contributor

| Action | Method | Description |
| --- | --- | --- |
| [Get Contributor](actions/get-contributor.md) | GET | Retrieves contributor from mittwald API. |
| [List Contributors](actions/list-contributors.md) | GET | Retrieves contributors from mittwald API. |

### Conversation Category

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversation Category](actions/get-conversation-category.md) | GET | Retrieves conversation category from mittwald API. |
| [List Conversation Categories](actions/list-conversation-categories.md) | GET | Retrieves conversation categories from mittwald API. |

### Conversation Preference

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Conversation Preferences](actions/get-customer-conversation-preferences.md) | GET | Retrieves customer conversation preferences from mittwald API. |

### Cronjob

| Action | Method | Description |
| --- | --- | --- |
| [List Project Cronjobs](actions/list-project-cronjobs.md) | GET | Retrieves project cronjobs from mittwald API. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves customer from mittwald API. |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from mittwald API. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [List Project MySQL Databases](actions/list-project-mysql-databases.md) | GET | Retrieves project MySQL databases from mittwald API. |
| [List Project Redis Databases](actions/list-project-redis-databases.md) | GET | Retrieves project Redis databases from mittwald API. |

### Delivery Box

| Action | Method | Description |
| --- | --- | --- |
| [List Project Delivery Boxes](actions/list-project-delivery-boxes.md) | GET | Retrieves project delivery boxes from mittwald API. |

### Dns Zone

| Action | Method | Description |
| --- | --- | --- |
| [List Project DNS Zones](actions/list-project-dns-zones.md) | GET | Retrieves project DNS zones from mittwald API. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [List Project Domains](actions/list-project-domains.md) | GET | Retrieves project domains from mittwald API. |

### Domain Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [List Domain Suggestions](actions/list-domain-suggestions.md) | GET | Retrieves AI-powered domain suggestions from mittwald API. |

### Domain Tld

| Action | Method | Description |
| --- | --- | --- |
| [List Domain TLDs](actions/list-domain-tlds.md) | GET | Retrieves domain TLDs from mittwald API. |

### Emails

| Action | Method | Description |
| --- | --- | --- |
| [Get Mail Address](actions/get-mail-address.md) | GET | Retrieves mail address from mittwald API. |
| [List Mail Addresses](actions/list-mail-addresses.md) | GET | Retrieves mail addresses from mittwald API. |
| [List Project Mail Addresses](actions/list-project-mail-addresses.md) | GET | Retrieves project mail addresses from mittwald API. |

### Extension

| Action | Method | Description |
| --- | --- | --- |
| [Get Extension](actions/get-extension.md) | GET | Retrieves extension from mittwald API. |
| [Get Project Extension](actions/get-project-extension.md) | GET | Retrieves project extension from mittwald API. |
| [List Extensions](actions/list-extensions.md) | GET | Retrieves extensions from mittwald API. |

### Extension Chargability

| Action | Method | Description |
| --- | --- | --- |
| [Get Extension Chargability](actions/get-extension-chargability.md) | GET | Retrieves whether an extension is chargeable from mittwald API. |

### File Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get File Metadata](actions/get-file-metadata.md) | GET | Retrieves file metadata from mittwald API. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get Project File Content](actions/get-project-file-content.md) | GET | Retrieves project file content from mittwald API. |
| [Get Project File Info](actions/get-project-file-info.md) | GET | Retrieves project file information from mittwald API. |

### Filesystem Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Filesystem Disk Usage](actions/get-project-filesystem-disk-usage.md) | GET | Retrieves project filesystem disk usage from mittwald API. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [List Project Filesystem Directories](actions/list-project-filesystem-directories.md) | GET | Retrieves project filesystem directories from mittwald API. |

### Ingress

| Action | Method | Description |
| --- | --- | --- |
| [Get Ingress](actions/get-ingress.md) | GET | Retrieves ingress from mittwald API. |
| [List Ingresses](actions/list-ingresses.md) | GET | Retrieves ingresses from mittwald API. |
| [List Project Ingresses](actions/list-project-ingresses.md) | GET | Retrieves project ingresses from mittwald API. |

### Invitations

| Action | Method | Description |
| --- | --- | --- |
| [List Project Invites](actions/list-project-invites.md) | GET | Retrieves project invites from mittwald API. |

### Invoice Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Invoice Settings](actions/get-customer-invoice-settings.md) | GET | Retrieves customer invoice settings from mittwald API. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Invoices](actions/list-customer-invoices.md) | GET | Retrieves customer invoices from mittwald API. |

### Jwt Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Project JWT](actions/get-project-jwt.md) | GET | Retrieves a project JWT token from mittwald API. |

### Legal Competence

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Legal Competence](actions/get-customer-legal-competence.md) | GET | Retrieves a customer's legal competence status from mittwald API. |

### Mail Address Backup

| Action | Method | Description |
| --- | --- | --- |
| [List Mail Address Backups](actions/list-mail-address-backups.md) | GET | Retrieves mail address backups from mittwald API. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Membership](actions/get-customer-membership.md) | GET | Retrieves customer membership from mittwald API. |
| [Get Project Membership](actions/get-project-membership.md) | GET | Retrieves project membership from mittwald API. |
| [Get Project Self Membership](actions/get-project-self-membership.md) | GET | Retrieves your project membership from mittwald API. |
| [List All Customer Memberships](actions/list-all-customer-memberships.md) | GET | Retrieves all customer memberships from mittwald API. |
| [List Customer Memberships](actions/list-customer-memberships.md) | GET | Retrieves customer memberships from mittwald API. |
| [List Project Memberships](actions/list-project-memberships.md) | GET | Retrieves project memberships from mittwald API. |
| [List Project Memberships For Project](actions/list-project-memberships-for-project.md) | GET | Retrieves project memberships for a project from mittwald API. |

### Mfa Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Self MFA Status](actions/get-self-mfa-status.md) | GET | Retrieves your MFA status from mittwald API. |

### Mysql Version

| Action | Method | Description |
| --- | --- | --- |
| [List MySQL Versions](actions/list-mysql-versions.md) | GET | Retrieves MySQL versions from mittwald API. |

### Newsletter Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get Newsletter Subscription](actions/get-newsletter-subscription.md) | GET | Retrieves newsletter subscription status from mittwald API. |

### Notification Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Notification Unread Counts](actions/get-notification-unread-counts.md) | GET | Retrieves unread notification counts from mittwald API. |

### Notification Counts

| Action | Method | Description |
| --- | --- | --- |
| [Get Notification Unread Counts Alias](actions/get-notification-unread-counts-alias.md) | GET | Retrieves unread notification counts from mittwald API. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves unread notifications from mittwald API. |

### Orders

| Action | Method | Description |
| --- | --- | --- |
| [List Customer Extension Orders](actions/list-customer-extension-orders.md) | GET | Retrieves customer extension orders from mittwald API. |
| [List Customer Orders](actions/list-customer-orders.md) | GET | Retrieves customer orders from mittwald API. |
| [List Project Extension Orders](actions/list-project-extension-orders.md) | GET | Retrieves project extension orders from mittwald API. |
| [List Project Orders](actions/list-project-orders.md) | GET | Retrieves project orders from mittwald API. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Billing Portal](actions/get-customer-billing-portal.md) | GET | Retrieves a customer billing portal link from mittwald API. |
| [List Project Page Insights](actions/list-project-page-insights.md) | GET | Retrieves project page insights from mittwald API. |

### Password Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Password Updated At](actions/get-password-updated-at.md) | GET | Retrieves your latest password change timestamp from mittwald API. |

### Project License

| Action | Method | Description |
| --- | --- | --- |
| [List Project Licenses](actions/list-project-licenses.md) | GET | Retrieves project licenses from mittwald API. |

### Project Service

| Action | Method | Description |
| --- | --- | --- |
| [List Project Services](actions/list-project-services.md) | GET | Retrieves project services from mittwald API. |

### Project Stack

| Action | Method | Description |
| --- | --- | --- |
| [List Project Stacks](actions/list-project-stacks.md) | GET | Retrieves project stacks from mittwald API. |

### Project Volume

| Action | Method | Description |
| --- | --- | --- |
| [List Project Volumes](actions/list-project-volumes.md) | GET | Retrieves project volumes from mittwald API. |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/get-current-user.md) | GET | Retrieves projects from mittwald API. |
| [Get Project](actions/get-project.md) | GET | Retrieves project from mittwald API. |

### Redis Version

| Action | Method | Description |
| --- | --- | --- |
| [List Redis Versions](actions/list-redis-versions.md) | GET | Retrieves Redis versions from mittwald API. |

### Registry

| Action | Method | Description |
| --- | --- | --- |
| [List Project Registries](actions/list-project-registries.md) | GET | Retrieves project registries from mittwald API. |

### Server

| Action | Method | Description |
| --- | --- | --- |
| [Get Server](actions/get-server.md) | GET | Retrieves server from mittwald API. |
| [List Servers](actions/list-servers.md) | GET | Retrieves servers from mittwald API. |

### Storage Statistics

| Action | Method | Description |
| --- | --- | --- |
| [Get Project Storage Space Statistics](actions/get-project-storage-space-statistics.md) | GET | Retrieves project storage space statistics from mittwald API. |
| [Get Server Storage Space Statistics](actions/get-server-storage-space-statistics.md) | GET | Retrieves server storage statistics from mittwald API. |

### System Software

| Action | Method | Description |
| --- | --- | --- |
| [Get System Software](actions/get-system-software.md) | GET | Retrieves system software from mittwald API. |
| [List System Softwares](actions/list-system-softwares.md) | GET | Retrieves system softwares from mittwald API. |

### System Software Version

| Action | Method | Description |
| --- | --- | --- |
| [Get System Software Version](actions/get-system-software-version.md) | GET | Retrieves system software version from mittwald API. |
| [List System Software Versions](actions/list-system-software-versions.md) | GET | Retrieves system software versions from mittwald API. |

### Tld Contact Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get TLD Contact Schemas](actions/get-tld-contact-schemas.md) | GET | Retrieves TLD contact schemas from mittwald API. |

### User Feedback

| Action | Method | Description |
| --- | --- | --- |
| [List User Feedback](actions/list-user-feedback.md) | GET | Retrieves user feedback from mittwald API. |

### User Settings

| Action | Method | Description |
| --- | --- | --- |
| [Get User Settings](actions/get-user-settings.md) | GET | Retrieves user settings from mittwald API. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Self Personal Information](actions/get-self-personal-information.md) | GET | Retrieves your personal information from mittwald API. |
| [Get User](actions/get-user.md) | GET | Retrieves user from mittwald API. |
| [List Project SFTP Users](actions/list-project-sftp-users.md) | GET | Retrieves project SFTP users from mittwald API. |
| [List Project SSH Users](actions/list-project-ssh-users.md) | GET | Retrieves project SSH users from mittwald API. |

### Wallet

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer Wallet](actions/get-customer-wallet.md) | GET | Retrieves a customer's wallet from mittwald API. |

