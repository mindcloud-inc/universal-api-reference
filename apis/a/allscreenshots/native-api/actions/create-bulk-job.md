# Create Bulk Job with Allscreenshots

Creates a bulk screenshot job for multiple URLs in Allscreenshots.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/screenshots/bulk`
- **Base URL:** `https://api.allscreenshots.com`
- **Official documentation:** [Create Bulk Job](https://docs.allscreenshots.com/api-reference/bulk)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urls[]` | body | `array<object>` | yes | The list of capture requests to include in the bulk job. |
| `defaults` | body | `object` | no | Shared screenshot options applied to every URL unless overridden. |
| `webhookUrl` | body | `string` | no | Optional URL to notify when the bulk job completes. |
| `webhookSecret` | body | `string` | no | Optional secret used to sign webhook deliveries. |
