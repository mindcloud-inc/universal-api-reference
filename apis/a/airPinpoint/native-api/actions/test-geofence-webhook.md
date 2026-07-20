# Test Geofence Webhook with AirPinpoint

Sends a test geofence webhook from AirPinpoint.

## Endpoint

- **Method:** `POST`
- **Path:** `/geofences/{geofence_id}/test-webhook`
- **Base URL:** `https://api.airpinpoint.com/v1`
- **Official documentation:** [Test Geofence Webhook](https://airpinpoint.com/docs/webhooks)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `eventType` | body | `string` | yes |
| `geofence_id` | path | `string` | yes |
