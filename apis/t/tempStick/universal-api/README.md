# <img src="https://images.mindcloud.co/apps/icons/temp-stick_1776452327120.png" alt="Temp Stick logo" width="28" height="28"> Temp Stick: Universal API

Monitor Temp Stick sensors, alerts, reports, and user settings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tempStick/latest
- **Category:** IT Operations / Observability
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://tempstick.com/
- **Vendor API docs:** https://tempstickapi.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tempStick/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [Get Alert](actions/get-alert.md) | GET | Retrieves a specific alert from Temp Stick. |
| [List Alerts](actions/list-alerts.md) | GET | Retrieves all alerts in Temp Stick. |

### Email Report

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Reports](actions/get-email-reports.md) | GET | Retrieves Temp Stick email report settings and downloadable reports. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [List Sensor Notifications](actions/list-sensor-notifications.md) | GET | Retrieves the last seven days of notifications for a Temp Stick sensor. |
| [List User Notifications](actions/list-user-notifications.md) | GET | Retrieves the last seven days of Temp Stick user notifications. |

### Sensor

| Action | Method | Description |
| --- | --- | --- |
| [Get Sensor](actions/get-sensor.md) | GET | Retrieves settings for a specific Temp Stick sensor. |
| [List Sensors](actions/list-sensors.md) | GET | Retrieves all sensors assigned to the Temp Stick account. |
| [Update Sensor Settings](actions/update-sensor-settings.md) | PUT | Updates settings for an existing Temp Stick sensor. |

### Sensor Reading

| Action | Method | Description |
| --- | --- | --- |
| [Get Sensor Readings](actions/get-sensor-readings.md) | GET | Retrieves readings for a Temp Stick sensor over a selected period. |

### Timezone

| Action | Method | Description |
| --- | --- | --- |
| [List Timezones](actions/list-timezones.md) | GET | Retrieves the list of supported Temp Stick timezones. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current Temp Stick user details. |
| [Update User Display Preferences](actions/update-user-display-preferences.md) | PUT | Updates Temp Stick display preferences for the current user. |

