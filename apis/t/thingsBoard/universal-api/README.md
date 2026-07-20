# <img src="https://images.mindcloud.co/apps/icons/thingsboard_1775840992370.png" alt="ThingsBoard logo" width="28" height="28"> ThingsBoard: Universal API

Manage IoT devices, assets, dashboards, telemetry, and alarms

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/thingsBoard/latest
- **Category:** IT Operations / Observability
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://thingsboard.io
- **Vendor API docs:** https://thingsboard.io/docs/paas/reference/rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [Acknowledge Alarm](actions/acknowledge-alarm.md) | PUT | Acknowledges an alarm in ThingsBoard. |
| [Clear Alarm](actions/clear-alarm.md) | PUT | Clears an alarm in ThingsBoard. |
| [Get Alarm](actions/get-alarm.md) | GET | Retrieves an alarm from ThingsBoard. |
| [List Alarm Types](actions/list-alarm-types.md) | GET | Retrieves available alarm types from ThingsBoard. |
| [List Alarms](actions/list-alarms.md) | GET | Retrieves alarms for a specific entity from ThingsBoard. |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Delete Asset](actions/delete-asset.md) | DELETE | Deletes an asset from ThingsBoard. |
| [Get Asset](actions/get-asset.md) | GET | Retrieves an asset from ThingsBoard. |
| [Get Asset Info](actions/get-asset-info.md) | GET | Retrieves asset info from ThingsBoard. |
| [List Asset Infos](actions/list-asset-infos.md) | GET | Retrieves asset info records from ThingsBoard. |
| [Save Asset](actions/save-asset.md) | PUT | Creates or updates an asset in ThingsBoard. |

### Attribute

| Action | Method | Description |
| --- | --- | --- |
| [Get Attributes](actions/get-attributes.md) | GET | Retrieves attributes for a specific entity from ThingsBoard. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Get Customer](actions/get-customer.md) | GET | Retrieves a customer from ThingsBoard. |
| [Get Customer Info](actions/get-customer-info.md) | GET | Retrieves customer info from ThingsBoard. |
| [List Customer Infos](actions/list-customer-infos.md) | GET | Retrieves customer info records from ThingsBoard. |
| [Save Customer](actions/save-customer.md) | PUT | Creates or updates a customer in ThingsBoard. |

### Dashboards

| Action | Method | Description |
| --- | --- | --- |
| [Get Dashboard](actions/get-dashboard.md) | GET | Retrieves a dashboard with configuration from ThingsBoard. |
| [List Dashboards](actions/list-dashboards.md) | GET | Retrieves dashboard info records from ThingsBoard. |
| [Save Dashboard](actions/save-dashboard.md) | PUT | Creates or updates a dashboard in ThingsBoard. |

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Delete Device](actions/delete-device.md) | DELETE | Deletes a device from ThingsBoard. |
| [Get Device](actions/get-device.md) | GET | Retrieves a device from ThingsBoard. |
| [List Device Infos](actions/list-device-infos.md) | GET | Retrieves device info records from ThingsBoard. |
| [Save Device](actions/save-device.md) | PUT | Creates or updates a device in ThingsBoard. |

### Entity

| Action | Method | Description |
| --- | --- | --- |
| [Find Related Entities](actions/find-related-entities.md) | GET | Finds entities related to a record in ThingsBoard. |

### Relation

| Action | Method | Description |
| --- | --- | --- |
| [List Relation Infos](actions/list-relation-infos.md) | GET |  |
| [Save Relation](actions/save-relation.md) | PUT |  |

### Time

| Action | Method | Description |
| --- | --- | --- |
| [Get Time Series](actions/get-time-series.md) | GET | Retrieves latest time series values from ThingsBoard. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from ThingsBoard. |

