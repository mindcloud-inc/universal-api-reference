# mittwald: Native API Reference

A consolidated summary of mittwald's API configuration and 102 documented operations, with links to official documentation.

- **Official docs:** https://api.mittwald.de/v2/openapi.json
- **OpenAPI specification:** https://api.mittwald.de/v2/openapi.json
- **API base URL:** `https://api.mittwald.de`

## Authentication

### API Key

Authenticate mittwald requests with a bearer token generated from mStudio.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.mittwald.de/v2/openapi.json)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (102 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get App](actions/get-app.md) | `GET /v2/apps/:appId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get App Version](actions/get-app-version.md) | `GET /v2/apps/:appId/versions/:appVersionId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Article](actions/get-article.md) | `GET /v2/articles/:articleId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Contributor](actions/get-contributor.md) | `GET /v2/contributors/:contributorId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Conversation Category](actions/get-conversation-category.md) | `GET /v2/conversation-categories/:categoryId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Projects](actions/get-current-user.md) | `GET /v2/projects` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Customer](actions/get-customer.md) | `GET /v2/customers/:customerId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Customer AI Hosting](actions/get-customer-ai-hosting.md) | `GET /v2/customers/:customerId/ai-hosting` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Customer AI Hosting Key](actions/get-customer-ai-hosting-key.md) | `GET /v2/customers/:customerId/ai-hosting-keys/:keyId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Customer Billing Portal](actions/get-customer-billing-portal.md) | `GET /v2/customers/:customerId/billing-portal` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Customer Conversation Preferences](actions/get-customer-conversation-preferences.md) | `GET /v2/customers/:customerId/conversation-preferences` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Customer Invoice Settings](actions/get-customer-invoice-settings.md) | `GET /v2/customers/:customerId/invoice-settings` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Customer Legal Competence](actions/get-customer-legal-competence.md) | `GET /v2/customers/:customerId/legally-competent` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Customer Membership](actions/get-customer-membership.md) | `GET /v2/customer-memberships/:customerMembershipId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Customer Wallet](actions/get-customer-wallet.md) | `GET /v2/customers/:customerId/wallet` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Extension](actions/get-extension.md) | `GET /v2/extensions/:extensionId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Extension Chargability](actions/get-extension-chargability.md) | `GET /v2/extensions/:extensionId/contexts/:contextId/chargability` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get File Metadata](actions/get-file-metadata.md) | `GET /v2/files/:fileId/meta` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Ingress](actions/get-ingress.md) | `GET /v2/ingresses/:ingressId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Mail Address](actions/get-mail-address.md) | `GET /v2/mail-addresses/:mailAddressId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Mail Address Contract](actions/get-mail-address-contract.md) | `GET /v2/mail-addresses/:mailAddressId/contract` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Newsletter Subscription](actions/get-newsletter-subscription.md) | `GET /v2/newsletter-subscriptions/self` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Notification Unread Counts](actions/get-notification-unread-counts.md) | `GET /v2/notifications/unread-counts` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Notification Unread Counts Alias](actions/get-notification-unread-counts-alias.md) | `GET /v2/notification-unread-counts` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Password Updated At](actions/get-password-updated-at.md) | `GET /v2/users/self/credentials/password-updated-at` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Project](actions/get-project.md) | `GET /v2/projects/:projectId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Project AI Hosting](actions/get-project-ai-hosting.md) | `GET /v2/projects/:projectId/ai-hosting` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Project AI Hosting Key](actions/get-project-ai-hosting-key.md) | `GET /v2/projects/:projectId/ai-hosting-keys/:keyId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Project Contract](actions/get-project-contract.md) | `GET /v2/projects/:projectId/contract` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Project Extension](actions/get-project-extension.md) | `GET /v2/projects/:projectId/extensions/:extensionId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Project File Content](actions/get-project-file-content.md) | `GET /v2/projects/:projectId/filesystem-file-content` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Project File Info](actions/get-project-file-info.md) | `GET /v2/projects/:projectId/filesystem-files` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Project Filesystem Disk Usage](actions/get-project-filesystem-disk-usage.md) | `GET /v2/projects/:projectId/filesystem-disk-usage` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Project JWT](actions/get-project-jwt.md) | `GET /v2/projects/:projectId/jwt` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Project Membership](actions/get-project-membership.md) | `GET /v2/project-memberships/:projectMembershipId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Project Self Membership](actions/get-project-self-membership.md) | `GET /v2/projects/:projectId/memberships/self` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Project Storage Space Statistics](actions/get-project-storage-space-statistics.md) | `GET /v2/projects/:projectId/storage-space-statistics` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Self MFA Status](actions/get-self-mfa-status.md) | `GET /v2/users/self/credentials/mfa` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Self Personal Information](actions/get-self-personal-information.md) | `GET /v2/users/self/personal-information` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Server](actions/get-server.md) | `GET /v2/servers/:serverId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Server Contract](actions/get-server-contract.md) | `GET /v2/servers/:serverId/contract` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get Server Storage Space Statistics](actions/get-server-storage-space-statistics.md) | `GET /v2/servers/:serverId/storage-space-statistics` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get System Software](actions/get-system-software.md) | `GET /v2/system-softwares/:systemSoftwareId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get System Software Version](actions/get-system-software-version.md) | `GET /v2/system-softwares/:systemSoftwareId/versions/:systemSoftwareVersionId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get TLD Contact Schemas](actions/get-tld-contact-schemas.md) | `GET /v2/domain-tlds/:tld/contact-schemas` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get User](actions/get-user.md) | `GET /v2/users/:userId` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [Get User Settings](actions/get-user-settings.md) | `GET /v2/users/:userId/settings` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List All Customer Memberships](actions/list-all-customer-memberships.md) | `GET /v2/customer-memberships` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List App Version Update Candidates](actions/list-app-version-update-candidates.md) | `GET /v2/apps/:appId/versions/:baseAppVersionId/update-candidates` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List App Versions](actions/list-app-versions.md) | `GET /v2/apps/:appId/versions` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Apps](actions/list-apps.md) | `GET /v2/apps` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Articles](actions/list-articles.md) | `GET /v2/articles` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Contributors](actions/list-contributors.md) | `GET /v2/contributors` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Conversation Categories](actions/list-conversation-categories.md) | `GET /v2/conversation-categories` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Customer AI Hosting Keys](actions/list-customer-ai-hosting-keys.md) | `GET /v2/customers/:customerId/ai-hosting-keys` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Customer AI Hosting Models](actions/list-customer-ai-hosting-models.md) | `GET /v2/customers/:customerId/ai-hosting-models` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Customer Contracts](actions/list-customer-contracts.md) | `GET /v2/customers/:customerId/contracts` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Customer Extension Orders](actions/list-customer-extension-orders.md) | `GET /v2/customers/:customerId/extension-orders` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Customer Invoices](actions/list-customer-invoices.md) | `GET /v2/customers/:customerId/invoices` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Customer Memberships](actions/list-customer-memberships.md) | `GET /v2/customers/:customerId/memberships` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Customer Orders](actions/list-customer-orders.md) | `GET /v2/customers/:customerId/orders` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Customers](actions/list-customers.md) | `GET /v2/customers` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Domain Suggestions](actions/list-domain-suggestions.md) | `GET /v2/domain-suggestions` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Domain TLDs](actions/list-domain-tlds.md) | `GET /v2/domain-tlds` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Extensions](actions/list-extensions.md) | `GET /v2/extensions` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Ingresses](actions/list-ingresses.md) | `GET /v2/ingresses` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Mail Address Backups](actions/list-mail-address-backups.md) | `GET /v2/mail-addresses/:mailAddressId/backups` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Mail Addresses](actions/list-mail-addresses.md) | `GET /v2/mail-addresses/` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List MySQL Versions](actions/list-mysql-versions.md) | `GET /v2/mysql-versions` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Notifications](actions/list-notifications.md) | `GET /v2/notifications` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project AI Hosting Keys](actions/list-project-ai-hosting-keys.md) | `GET /v2/projects/:projectId/ai-hosting-keys` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project AI Hosting Models](actions/list-project-ai-hosting-models.md) | `GET /v2/projects/:projectId/ai-hosting-models` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project App Installations](actions/list-project-app-installations.md) | `GET /v2/projects/:projectId/app-installations` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Backup Schedules](actions/list-project-backup-schedules.md) | `GET /v2/projects/:projectId/backup-schedules` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Backups](actions/list-project-backups.md) | `GET /v2/projects/:projectId/backups` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Cronjobs](actions/list-project-cronjobs.md) | `GET /v2/projects/:projectId/cronjobs` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Delivery Boxes](actions/list-project-delivery-boxes.md) | `GET /v2/projects/:projectId/delivery-boxes` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project DNS Zones](actions/list-project-dns-zones.md) | `GET /v2/projects/:projectId/dns-zones` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Domains](actions/list-project-domains.md) | `GET /v2/projects/:projectId/domains` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Extension Orders](actions/list-project-extension-orders.md) | `GET /v2/projects/:projectId/extension-orders` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Filesystem Directories](actions/list-project-filesystem-directories.md) | `GET /v2/projects/:projectId/filesystem-directories` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Ingresses](actions/list-project-ingresses.md) | `GET /v2/projects/:projectId/ingresses` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Invites](actions/list-project-invites.md) | `GET /v2/projects/:projectId/invites` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Licenses](actions/list-project-licenses.md) | `GET /v2/projects/:projectId/licenses` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Mail Addresses](actions/list-project-mail-addresses.md) | `GET /v2/projects/:projectId/mail-addresses` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Memberships](actions/list-project-memberships.md) | `GET /v2/project-memberships` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Memberships For Project](actions/list-project-memberships-for-project.md) | `GET /v2/projects/:projectId/memberships` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project MySQL Databases](actions/list-project-mysql-databases.md) | `GET /v2/projects/:projectId/mysql-databases` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Orders](actions/list-project-orders.md) | `GET /v2/projects/:projectId/orders` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Page Insights](actions/list-project-page-insights.md) | `GET /v2/projects/:projectId/page-insights` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Redis Databases](actions/list-project-redis-databases.md) | `GET /v2/projects/:projectId/redis-databases` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Registries](actions/list-project-registries.md) | `GET /v2/projects/:projectId/registries` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Services](actions/list-project-services.md) | `GET /v2/projects/:projectId/services` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project SFTP Users](actions/list-project-sftp-users.md) | `GET /v2/projects/:projectId/sftp-users` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project SSH Users](actions/list-project-ssh-users.md) | `GET /v2/projects/:projectId/ssh-users` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Stacks](actions/list-project-stacks.md) | `GET /v2/projects/:projectId/stacks` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Project Volumes](actions/list-project-volumes.md) | `GET /v2/projects/:projectId/volumes` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Redis Versions](actions/list-redis-versions.md) | `GET /v2/redis-versions` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List Servers](actions/list-servers.md) | `GET /v2/servers` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List System Software Versions](actions/list-system-software-versions.md) | `GET /v2/system-softwares/:systemSoftwareId/versions` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List System Softwares](actions/list-system-softwares.md) | `GET /v2/system-softwares` | [docs](https://api.mittwald.de/v2/openapi.json) |
| [List User Feedback](actions/list-user-feedback.md) | `GET /v2/users/:userId/feedback` | [docs](https://api.mittwald.de/v2/openapi.json) |
