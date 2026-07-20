# Update Custom Status with Callbell

Updates an existing custom status in Callbell.

## Endpoint

- **Method:** `PUT`
- **Path:** `/custom_statuses/:uuid`
- **Base URL:** `https://api.callbell.eu/v1`
- **Official documentation:** [Update Custom Status](https://docs.callbell.eu/api/reference/custom_status_api/put_custom_status/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Updated name of the custom status. |
| `uuid` | path | `string` | yes | Unique identifier of the custom status to update. |
