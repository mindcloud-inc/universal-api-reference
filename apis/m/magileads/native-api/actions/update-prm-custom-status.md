# Update PRM Custom Status with Magileads

Updates an existing PRM custom status in Magileads.

## Endpoint

- **Method:** `PUT`
- **Path:** `/prm/status/custom/:status_id`
- **Base URL:** `https://app.api-magileads.net`
- **Official documentation:** [Update PRM Custom Status](https://api.magileads.net)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | The updated custom status color in hex. |
| `name` | body | `string` | no | The updated custom status name. |
| `status_id` | path | `number` | yes | The custom status ID. |
