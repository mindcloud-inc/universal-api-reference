# <img src="https://images.mindcloud.co/apps/icons/ubidots-icon_1778103710488.png" alt="Ubidots logo" width="28" height="28"> Ubidots: Universal API

Ubidots is an industrial IoT platform for managing devices, variables, dashboards, events, organizations, users, and time-series device data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ubidots/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ubidots.com
- **Vendor API docs:** https://docs.ubidots.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get all Devices](actions/get-all-devices.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ubidots/latest/actions/get-all-devices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Dashboard

| Action | Method | Description |
| --- | --- | --- |
| [Get all Dashboards](actions/get-all-dashboards.md) | GET |  |
| [Get Dashboard](actions/get-dashboard.md) | GET |  |

### Dashboard Model

| Action | Method | Description |
| --- | --- | --- |
| [Export Dashboard Model](actions/export-dashboard-model.md) | GET |  |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [Get all Devices](actions/get-all-devices.md) | GET |  |
| [Get Device](actions/get-device.md) | GET |  |
| [Get Organization Device](actions/get-organization-device.md) | GET |  |
| [Get Organization Devices](actions/get-organization-devices.md) | GET |  |

### Device Group

| Action | Method | Description |
| --- | --- | --- |
| [Get all Device Groups](actions/get-all-device-groups.md) | GET |  |
| [Get Device Group](actions/get-device-group.md) | GET |  |

### Device Type

| Action | Method | Description |
| --- | --- | --- |
| [Get all Device Types](actions/get-all-device-types.md) | GET |  |
| [Get Device Type](actions/get-device-type.md) | GET |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Get all Events](actions/get-all-events.md) | GET |  |
| [Get Event](actions/get-event.md) | GET |  |

### Event Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Event Log](actions/get-event-log.md) | GET |  |
| [Get Event Logs](actions/get-event-logs.md) | GET |  |

### Last Value

| Action | Method | Description |
| --- | --- | --- |
| [Get Device Last Values](actions/get-device-last-values.md) | GET |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get all Organizations](actions/get-all-organizations.md) | GET |  |
| [Get Organization](actions/get-organization.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get all Users](actions/get-all-users.md) | GET |  |
| [Get User](actions/get-user.md) | GET |  |

### Variable

| Action | Method | Description |
| --- | --- | --- |
| [Get all Variables](actions/get-all-variables.md) | GET |  |
| [Get Device Variable](actions/get-device-variable.md) | GET |  |
| [Get Device Variables](actions/get-device-variables.md) | GET |  |
| [Get Variable](actions/get-variable.md) | GET |  |

