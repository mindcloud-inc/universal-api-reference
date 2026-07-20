# List Known IPs with Control D

Retrieves known IPs from Control D.

## Endpoint

- **Method:** `GET`
- **Path:** `/access`
- **Base URL:** `https://api.controld.com`
- **Official documentation:** [List Known IPs](https://docs.controld.com/reference/get_access)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_id` | query | `string` | yes | (Required) Primary key of the device. |
