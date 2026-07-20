# Dotcom Monitor: Native API Reference

A consolidated summary of Dotcom Monitor's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://www.dotcom-monitor.com/wiki/knowledge-base-category/api/
- **API base URL:** `https://api.dotcom-monitor.com/config_api_v1`

## Authentication

### Monitoring Web API UID

Authenticates against the Dotcom-Monitor Web API by exchanging a Monitoring Web API UID for a cookie-backed session.

### Credentials

- **Web API UID:** `uid` · required · The Monitoring Web API Unique Identifier created under Manage > Integrations > New Integration > Monitoring Web API.

[Official authentication documentation](https://www.dotcom-monitor.com/wiki/knowledge-base/authentication/)

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | `POST /login` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/authentication/) |
| [Delete Device](actions/delete-device.md) | `DELETE /device/:deviceId` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/delete-device/) |
| [Delete Task](actions/delete-task.md) | `DELETE /task/:taskId` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/delete-task/) |
| [Disable Alerts for Device](actions/disable-alerts-for-device.md) | `POST /device/:deviceId/DisableAlert` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/api-disable-alerts-for-a-device/) |
| [Get Audit Event Info](actions/get-audit-event-info.md) | `GET /audit/object/:sample_id` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/get-audit-event-info/) |
| [Get Device Info](actions/get-device-info.md) | `GET /device/:deviceId` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/get-device-info/) |
| [Get Filter Info](actions/get-filter-info.md) | `GET /filter/:filter_id` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/get-specific-filter-info/) |
| [Get Notification Group Info](actions/get-notification-group-info.md) | `GET /group/:group_id` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/get-notification-group-info/) |
| [Get Task Info](actions/get-task-info.md) | `GET /task/:taskId` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/get-task-info/) |
| [List Alert Templates](actions/list-alert-templates.md) | `GET /templates` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/get-list-of-notification-templates/) |
| [List Audit Objects](actions/list-audit-objects.md) | `GET /audit/list` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/get-list-of-audit-objects/) |
| [List Crypts](actions/list-crypts.md) | `GET /securevaults` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/api-get-list-of-crypts/) |
| [List Devices by Platform](actions/list-devices-by-platform.md) | `GET /devices/:platform_name` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/get-device-list-by-platform/) |
| [List Filters](actions/list-filters.md) | `GET /filters` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/get-list-of-filters/) |
| [List Monitoring Frequencies](actions/list-monitoring-frequencies.md) | `GET /frequencies/:platform_name` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/frequencies-list/) |
| [List Monitoring Locations](actions/list-monitoring-locations.md) | `GET /locations/:platform_name` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/monitoring-agents/) |
| [List Monitoring Platforms](actions/list-monitoring-platforms.md) | `GET /platforms` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/platforms/) |
| [List Notification Groups](actions/list-notification-groups.md) | `GET /groups` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/get-list-of-notification-groups/) |
| [List Schedulers](actions/list-schedulers.md) | `GET /schedulers` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/get-list-of-schedulers/) |
| [List Tasks by Device](actions/list-tasks-by-device.md) | `GET /device/:deviceId/tasks` | [docs](https://www.dotcom-monitor.com/wiki/knowledge-base/get-task-list-by-device/) |
