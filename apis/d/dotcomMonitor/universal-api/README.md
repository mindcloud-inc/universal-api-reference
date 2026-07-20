# <img src="https://images.mindcloud.co/apps/icons/dotcom-monitor_1775079655840.png" alt="Dotcom Monitor logo" width="28" height="28"> Dotcom Monitor: Universal API

Dotcom Monitor lets teams manage monitoring devices, tasks, alerts, filters, notification groups, and related configuration through the Dotcom-Monitor Web API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dotcomMonitor/latest
- **Category:** IT Operations / Observability
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dotcom-monitor.com/
- **Vendor API docs:** https://www.dotcom-monitor.com/wiki/knowledge-base-category/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Authenticate](actions/authenticate.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotcomMonitor/latest/actions/authenticate?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Audit Logs

| Action | Method | Description |
| --- | --- | --- |
| [Get Audit Event Info](actions/get-audit-event-info.md) | GET | Retrieves audit event details from Dotcom Monitor. |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Filter Info](actions/get-filter-info.md) | GET | Retrieves filter details from Dotcom Monitor. |
| [List Audit Objects](actions/list-audit-objects.md) | GET | Retrieves audit objects from Dotcom Monitor. |
| [List Crypts](actions/list-crypts.md) | GET | Retrieves secure vault crypts from Dotcom Monitor. |
| [List Filters](actions/list-filters.md) | GET | Retrieves saved filters from Dotcom Monitor. |
| [List Monitoring Frequencies](actions/list-monitoring-frequencies.md) | GET | Retrieves monitoring frequencies for a platform from Dotcom Monitor. |
| [List Monitoring Platforms](actions/list-monitoring-platforms.md) | GET | Retrieves monitoring platforms from Dotcom Monitor. |
| [List Schedulers](actions/list-schedulers.md) | GET | Retrieves configured schedulers from Dotcom Monitor. |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Delete Device](actions/delete-device.md) | DELETE | Deletes an existing device from Dotcom Monitor. |
| [Disable Alerts for Device](actions/disable-alerts-for-device.md) | PUT | Disables alerts for a device in Dotcom Monitor temporarily. |
| [Get Device Info](actions/get-device-info.md) | GET | Retrieves device details from Dotcom Monitor. |
| [List Devices by Platform](actions/list-devices-by-platform.md) | GET | Retrieves devices for a monitoring platform from Dotcom Monitor. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Notification Group Info](actions/get-notification-group-info.md) | GET | Retrieves notification group details from Dotcom Monitor. |
| [List Notification Groups](actions/list-notification-groups.md) | GET | Retrieves notification groups from Dotcom Monitor. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Monitoring Locations](actions/list-monitoring-locations.md) | GET | Retrieves monitoring locations for a platform from Dotcom Monitor. |

### Sessions

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | GET | Authenticates with Dotcom Monitor and starts a session. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Dotcom Monitor. |
| [Get Task Info](actions/get-task-info.md) | GET | Retrieves task details from Dotcom Monitor. |
| [List Tasks by Device](actions/list-tasks-by-device.md) | GET | Retrieves tasks for a device from Dotcom Monitor. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Alert Templates](actions/list-alert-templates.md) | GET | Retrieves alert templates from Dotcom Monitor. |

