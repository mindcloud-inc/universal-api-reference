# <img src="https://images.mindcloud.co/apps/icons/rachio-smart-hose-timer_1776367987510.png" alt="Rachio Smart Hose Timer logo" width="28" height="28"> Rachio Smart Hose Timer: Universal API

Manage smart hose timers, valves, schedules, and watering events

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/rachioSmartHoseTimer/latest
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://rachio.com/products/smart-hose-timer/
- **Vendor API docs:** https://rachio.readme.io/reference/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Person Info](actions/get-current-person-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rachioSmartHoseTimer/latest/actions/get-current-person-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Devices

| Action | Method | Description |
| --- | --- | --- |
| [Get Controller Device](actions/get-controller-device.md) | GET | Retrieves controller device details from Rachio. |
| [List Base Stations](actions/list-base-stations.md) | GET | Retrieves smart hose timer base stations from Rachio. |

### Events

| Action | Method | Description |
| --- | --- | --- |
| [List Device Events](actions/list-device-events.md) | GET | Retrieves device event records from Rachio. |
| [List Notification Webhook Event Types](actions/list-notification-webhook-event-types.md) | GET | Retrieves notification webhook event types from Rachio. |
| [List Webhook Event Types](actions/list-webhook-event-types.md) | GET | Retrieves webhook event types from Rachio. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Find Property By Entity](actions/find-property-by-entity.md) | GET | Finds a property in Rachio by entity ID. |
| [Get Property](actions/get-property.md) | GET | Retrieves property details from your Rachio account. |
| [List Properties](actions/list-properties.md) | GET | Retrieves property records from your Rachio account. |

### Person

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Person Info](actions/get-current-person-info.md) | GET | Retrieves the current person identifier from Rachio. |

### Programs

| Action | Method | Description |
| --- | --- | --- |
| [Create Planned Run Skip Overrides](actions/create-planned-run-skip-overrides.md) | POST | Creates planned run skip overrides in Rachio. |
| [Create Program V2](actions/create-program-v2.md) | POST | Creates a new program in Rachio. |
| [Create Skip Overrides](actions/create-skip-overrides.md) | POST | Creates program skip overrides in Rachio. |
| [List Programs V2](actions/list-programs-v2.md) | GET | Retrieves program records from your Rachio account. |
| [Update Program V2](actions/update-program-v2.md) | PUT | Updates an existing program in Rachio. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Device Forecast](actions/get-device-forecast.md) | GET | Retrieves a device forecast from Rachio. |
| [Get Valve Day Views](actions/get-valve-day-views.md) | GET | Retrieves valve day views from Rachio. |

### Schedules

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Schedule](actions/get-current-schedule.md) | GET | Retrieves the current schedule from Rachio. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Person](actions/get-person.md) | GET | Retrieves person details from your Rachio account. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Notification Webhook](actions/create-notification-webhook.md) | POST | Creates a notification webhook for a Rachio device. |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Rachio. |
| [Delete Notification Webhook](actions/delete-notification-webhook.md) | DELETE | Deletes an existing notification webhook from Rachio. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Rachio. |
| [Get Notification Webhook](actions/get-notification-webhook.md) | GET | Retrieves a notification webhook from Rachio. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a configured webhook from Rachio. |
| [List Device Webhooks](actions/list-device-webhooks.md) | GET | Retrieves webhooks for a specific Rachio device. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves configured webhooks from your Rachio account. |
| [Update Notification Webhook](actions/update-notification-webhook.md) | PUT | Updates an existing notification webhook in Rachio. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Rachio. |

