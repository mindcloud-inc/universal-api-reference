# Upload IP Data with Chargeblast

Uploads IP data to Chargeblast.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/track`
- **Base URL:** `https://api.chargeblast.com`
- **Official documentation:** [Upload IP Data](https://docs.chargeblast.com/api-reference/sync-data/track)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The customer email associated with the IP signal. |
| `ip` | body | `string` | yes | The customer IP address. |
