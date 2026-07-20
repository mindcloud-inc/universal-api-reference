# Send Reminder with Eversign

Sends a signer reminder in Eversign.

## Endpoint

- **Method:** `POST`
- **Path:** `/send_reminder`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Send Reminder](https://eversign.com/api/documentation/methods)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `document_hash` | body | `string` | yes |
| `signer_id` | body | `string` | yes |
