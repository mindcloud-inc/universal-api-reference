# Update Status with Ellipsend

Updates an existing status in Ellipsend.

## Endpoint

- **Method:** `PUT`
- **Path:** `/status/[:status_id]`
- **Base URL:** `https://api.ellipsend.com/v1`
- **Official documentation:** [Update Status](https://api.ellipsend.com/v1/docs#/Status/put_status__status_id_)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status_id` | path | `number` | yes | The status ID. |
| `status` | body | `string` | yes | The new status value. |
