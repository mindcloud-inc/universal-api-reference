# <img src="https://images.mindcloud.co/apps/icons/air-pinpoint_1775502804627.png" alt="AirPinpoint logo" width="28" height="28"> AirPinpoint: Universal API

Track AirTags and other Find My-enabled devices, view location history, manage geofences, test webhook delivery, and generate temporary share links with the AirPinpoint API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/airPinpoint/latest
- **Category:** Support / Field Service
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://airpinpoint.com
- **Vendor API docs:** https://airpinpoint.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Trackables](actions/list-trackables.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airPinpoint/latest/actions/list-trackables?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Geofence

| Action | Method | Description |
| --- | --- | --- |
| [Create Geofence](actions/create-geofence.md) | POST | Creates a geofence for AirPinpoint trackables. |
| [Delete Geofence](actions/delete-geofence.md) | DELETE | Deletes an existing geofence from AirPinpoint. |
| [List Geofences](actions/list-geofences.md) | GET | Retrieves configured geofences for AirPinpoint trackables. |
| [Update Geofence](actions/update-geofence.md) | PUT | Updates an existing geofence in AirPinpoint. |

### Share Link

| Action | Method | Description |
| --- | --- | --- |
| [Generate Share Link](actions/generate-share-link.md) | POST | Creates a temporary share link for a trackable in AirPinpoint. |

### Trackable

| Action | Method | Description |
| --- | --- | --- |
| [Get Trackable](actions/get-trackable.md) | GET | Retrieves details for a trackable in AirPinpoint. |
| [List Trackables](actions/list-trackables.md) | GET | Retrieves trackable devices linked to AirPinpoint. |

### Trackable Battery

| Action | Method | Description |
| --- | --- | --- |
| [Get Trackable Battery](actions/get-trackable-battery.md) | GET | Retrieves battery status for a trackable in AirPinpoint. |
| [Reset Trackable Battery](actions/reset-trackable-battery.md) | PUT | Resets the battery counter for a trackable in AirPinpoint. |

### Trackable Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Trackable Locations](actions/get-trackable-locations.md) | GET | Retrieves location data for a trackable in AirPinpoint. |

### Webhook Test

| Action | Method | Description |
| --- | --- | --- |
| [Test Geofence Webhook](actions/test-geofence-webhook.md) | POST | Sends a test geofence webhook from AirPinpoint. |

