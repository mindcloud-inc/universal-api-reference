# Create PRM Custom Status with Magileads

Creates a new PRM custom status in Magileads.

## Endpoint

- **Method:** `POST`
- **Path:** `/prm/status/custom`
- **Base URL:** `https://app.api-magileads.net`
- **Official documentation:** [Create PRM Custom Status](https://api.magileads.net)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The custom status name. |
| `color` | body | `string` | no | The custom status color in hex. |
