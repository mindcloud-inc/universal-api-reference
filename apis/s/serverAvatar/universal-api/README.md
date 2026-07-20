# <img src="https://images.mindcloud.co/apps/icons/server-avatar_1776367813742.png" alt="ServerAvatar logo" width="28" height="28"> ServerAvatar: Universal API

Manage servers, applications, databases, backups, and SSL certificates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/serverAvatar/latest
- **Category:** IT Operations / DevOps
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://app.serveravatar.com
- **Vendor API docs:** https://serveravatar.com/api-docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/serverAvatar/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [List Server Alerts](actions/list-server-alerts.md) | GET | Retrieves server alerts from ServerAvatar. |

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Get Application](actions/get-application.md) | GET | Retrieves an application from ServerAvatar. |
| [List Organization Applications](actions/list-organization-applications.md) | GET | Retrieves organization applications from ServerAvatar. |
| [List Server Applications](actions/list-server-applications.md) | GET | Retrieves server applications from ServerAvatar. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Databases](actions/list-organization-databases.md) | GET | Retrieves organization databases from ServerAvatar. |
| [List Server Databases](actions/list-server-databases.md) | GET | Retrieves server databases from ServerAvatar. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from ServerAvatar. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from ServerAvatar. |

### Services

| Action | Method | Description |
| --- | --- | --- |
| [List Server Services](actions/list-server-services.md) | GET | Retrieves server services from ServerAvatar. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Application Log Sizes](actions/get-application-log-sizes.md) | GET | Retrieves application log sizes from ServerAvatar. |
| [Get Application SFTP Credentials](actions/get-application-sftp-credentials.md) | GET | Retrieves application SFTP credentials from ServerAvatar. |
| [Get Firewall Status](actions/get-firewall-status.md) | GET | Retrieves firewall details from ServerAvatar. |
| [Get Server](actions/get-server.md) | GET | Retrieves a server from ServerAvatar. |
| [Get Server Logs](actions/get-server-logs.md) | GET | Retrieves server logs from ServerAvatar. |
| [Get Server Resource Usage](actions/get-server-resource-usage.md) | GET | Retrieves server resource usage from ServerAvatar. |
| [Get Server Status](actions/get-server-status.md) | GET | Retrieves server status from ServerAvatar. |
| [Get Server Summary](actions/get-server-summary.md) | GET | Retrieves a server summary from ServerAvatar. |
| [Get SSL Certificate](actions/get-ssl-certificate.md) | GET | Retrieves an SSL certificate from ServerAvatar. |
| [List Application Domains](actions/list-application-domains.md) | GET | Retrieves application domains from ServerAvatar. |
| [List Backup Presets](actions/list-backup-presets.md) | GET | Retrieves backup presets from ServerAvatar. |
| [List Backups](actions/list-backups.md) | GET | Retrieves backups from ServerAvatar. |
| [List Connected Server Providers](actions/list-connected-server-providers.md) | GET | Retrieves connected server providers from ServerAvatar. |
| [List Cronjobs](actions/list-cronjobs.md) | GET | Retrieves cronjobs from ServerAvatar. |
| [List Git Providers](actions/list-git-providers.md) | GET | Retrieves Git providers from ServerAvatar. |
| [List Server Provider Regions](actions/list-server-provider-regions.md) | GET | Retrieves server provider regions from ServerAvatar. |
| [List Servers](actions/list-servers.md) | GET | Retrieves servers from ServerAvatar. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Application Users](actions/list-application-users.md) | GET | Retrieves application users from ServerAvatar. |
| [List Database Users](actions/list-database-users.md) | GET | Retrieves database users from ServerAvatar. |
| [List Organization Members](actions/list-organization-members.md) | GET | Retrieves organization members from ServerAvatar. |

