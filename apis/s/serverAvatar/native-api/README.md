# ServerAvatar: Native API Reference

A consolidated summary of ServerAvatar's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://serveravatar.com/api-docs/
- **API base URL:** `https://api.serveravatar.com`

## Authentication

### API Key

Connect with a ServerAvatar API access key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://serveravatar.com/docs/account-management/api-access/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Application](actions/get-application.md) | `GET /organizations/{{organization}}/servers/{{server}}/applications/{{application}}` | [docs](https://serveravatar.com/api-docs/endpoint/application/show.html) |
| [Get Application Log Sizes](actions/get-application-log-sizes.md) | `GET /organizations/{{organization}}/servers/{{server}}/applications/{{application}}/log-sizes` | [docs](https://serveravatar.com/api-docs/endpoint/application/logs.html) |
| [Get Application SFTP Credentials](actions/get-application-sftp-credentials.md) | `GET /organizations/{{organization}}/servers/{{server}}/applications/{{application}}/sftp` | [docs](https://serveravatar.com/api-docs/endpoint/application/sftp-credentials.html) |
| [Get Firewall Status](actions/get-firewall-status.md) | `GET /organizations/{{organization}}/servers/{{server}}/firewall` | [docs](https://serveravatar.com/api-docs/endpoint/firewall/) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/{{organization}}` | [docs](https://serveravatar.com/api-docs/endpoint/organization/show.html) |
| [Get Server](actions/get-server.md) | `GET /organizations/{{organization}}/servers/{{server}}` | [docs](https://serveravatar.com/api-docs/endpoint/server/show.html) |
| [Get Server Logs](actions/get-server-logs.md) | `GET /organizations/{{organization}}/servers/{{server}}/logs` | [docs](https://serveravatar.com/api-docs/endpoint/server/logs.html) |
| [Get Server Resource Usage](actions/get-server-resource-usage.md) | `GET /organizations/{{organization}}/servers/{{server}}/usage` | [docs](https://serveravatar.com/api-docs/endpoint/server/resources-usage.html) |
| [Get Server Status](actions/get-server-status.md) | `GET /organizations/{{organization}}/servers/{{server}}/status` | [docs](https://serveravatar.com/api-docs/endpoint/server/status.html) |
| [Get Server Summary](actions/get-server-summary.md) | `GET /organizations/{{organization}}/servers/{{server}}/summary` | [docs](https://serveravatar.com/api-docs/endpoint/server/summary.html) |
| [Get SSL Certificate](actions/get-ssl-certificate.md) | `GET /organizations/{{organization}}/servers/{{server}}/applications/{{application}}/ssl` | [docs](https://serveravatar.com/api-docs/endpoint/ssl/show.html) |
| [List Application Domains](actions/list-application-domains.md) | `GET /organizations/{{organization}}/servers/{{server}}/applications/{{application}}/application-domains` | [docs](https://serveravatar.com/api-docs/endpoint/application-domain/) |
| [List Application Users](actions/list-application-users.md) | `GET /organizations/{{organization}}/servers/{{server}}/system-users` | [docs](https://serveravatar.com/api-docs/endpoint/application-user/) |
| [List Backup Presets](actions/list-backup-presets.md) | `GET /organizations/{{organization}}/servers/{{server}}/backups/presets` | [docs](https://serveravatar.com/api-docs/endpoint/backup/preset.html) |
| [List Backups](actions/list-backups.md) | `GET /organizations/{{organization}}/backups` | [docs](https://serveravatar.com/api-docs/endpoint/backup/) |
| [List Connected Server Providers](actions/list-connected-server-providers.md) | `GET /organizations/{{organization}}/cloud-server-providers` | [docs](https://serveravatar.com/api-docs/endpoint/server-provider/) |
| [List Cronjobs](actions/list-cronjobs.md) | `GET /organizations/{{organization}}/servers/{{server}}/cronjobs` | [docs](https://serveravatar.com/api-docs/endpoint/cronjob/) |
| [List Database Users](actions/list-database-users.md) | `GET /organizations/{{organization}}/servers/{{server}}/databases/{{database}}/database-users` | [docs](https://serveravatar.com/api-docs/endpoint/database-user/) |
| [List Git Providers](actions/list-git-providers.md) | `GET /organizations/{{organization}}/git-providers` | [docs](https://serveravatar.com/api-docs/endpoint/git-provider/) |
| [List Organization Applications](actions/list-organization-applications.md) | `GET /organizations/{{organization}}/applications` | [docs](https://serveravatar.com/api-docs/endpoint/application/) |
| [List Organization Databases](actions/list-organization-databases.md) | `GET /organizations/{{organization}}/databases` | [docs](https://serveravatar.com/api-docs/endpoint/database/) |
| [List Organization Members](actions/list-organization-members.md) | `GET /organizations/{{organization}}/members` | [docs](https://serveravatar.com/api-docs/endpoint/organization/member.html) |
| [List Organizations](actions/list-organizations.md) | `GET /organizations` | [docs](https://serveravatar.com/api-docs/endpoint/organization/) |
| [List Server Alerts](actions/list-server-alerts.md) | `GET /organizations/{{organization}}/servers/{{server}}/alert` | [docs](https://serveravatar.com/api-docs/endpoint/server/alerts.html) |
| [List Server Applications](actions/list-server-applications.md) | `GET /organizations/{{organization}}/servers/{{server}}/applications` | [docs](https://serveravatar.com/api-docs/endpoint/application/) |
| [List Server Databases](actions/list-server-databases.md) | `GET /organizations/{{organization}}/servers/{{server}}/databases` | [docs](https://serveravatar.com/api-docs/endpoint/database/) |
| [List Server Provider Regions](actions/list-server-provider-regions.md) | `GET /organizations/{{organization}}/cloud-server-providers/{{cloudServerProvider}}/regions` | [docs](https://serveravatar.com/api-docs/endpoint/server-provider/region.html) |
| [List Server Services](actions/list-server-services.md) | `GET /organizations/{{organization}}/servers/{{server}}/services` | [docs](https://serveravatar.com/api-docs/endpoint/server/services.html) |
| [List Servers](actions/list-servers.md) | `GET /organizations/{{organization}}/servers` | [docs](https://serveravatar.com/api-docs/endpoint/server/) |
