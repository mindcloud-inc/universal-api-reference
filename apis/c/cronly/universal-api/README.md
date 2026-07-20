# <img src="https://images.mindcloud.co/apps/icons/cronly_1775150351419.png" alt="Cronly logo" width="28" height="28"> Cronly: Universal API

Monitor cron jobs, manage projects, and receive notifications for failures and recoveries.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cronly/latest
- **Category:** IT Operations / Observability
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cronly.app/
- **Vendor API docs:** https://docs.cronly.app/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cronly/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Company](actions/get-company.md) | GET |  |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Create Server](actions/create-server.md) | POST |  |
| [Get Server](actions/get-server.md) | GET |  |
| [List Servers](actions/list-servers.md) | GET |  |

### Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create SSL Certificate Monitor](actions/create-ssl-certificate-monitor.md) | POST |  |
| [Delete SSL Certificate Monitor](actions/delete-ssl-certificate-monitor.md) | DELETE |  |
| [Get SSL Certificate Monitor](actions/get-ssl-certificate-monitor.md) | GET |  |
| [List SSL Certificate Monitors](actions/list-ssl-certificate-monitors.md) | GET |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Create Backup](actions/create-backup.md) | POST |  |
| [Delete Backup](actions/delete-backup.md) | DELETE |  |
| [Get Backup](actions/get-backup.md) | GET |  |
| [List Backups](actions/list-backups.md) | GET |  |

### Monitors

| Action | Method | Description |
| --- | --- | --- |
| [Create Job Monitor](actions/create-job-monitor.md) | POST |  |
| [Delete Job Monitor](actions/delete-job-monitor.md) | DELETE |  |
| [Get Job Monitor](actions/get-job-monitor.md) | GET |  |
| [List Job Monitors](actions/list-job-monitors.md) | GET |  |
| [Send Monitor Pulse](actions/send-monitor-pulse.md) | PUT |  |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [List Notifications](actions/list-notifications.md) | GET |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |
| [Delete Project](actions/delete-project.md) | DELETE |  |
| [Get Project](actions/get-project.md) | GET |  |
| [List Projects](actions/list-projects.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET |  |
| [List Users](actions/list-users.md) | GET |  |

