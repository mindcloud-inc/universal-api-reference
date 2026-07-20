# Cancel Pin Request with Pinata

Deletes an existing pin request from Pinata.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/files/public/pin_by_cid/:id`
- **Base URL:** `https://api.pinata.cloud`
- **Official documentation:** [Cancel Pin Request](https://docs.pinata.cloud/api-reference/endpoint/cancel-pin-by-cid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | ID of the pin-by-CID request to cancel. |
