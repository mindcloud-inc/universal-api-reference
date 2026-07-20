# Create dashboard with 2Smart Cloud

## Endpoint

- **Method:** `POST`
- **Path:** `/vendor/dashboards`
- **Base URL:** `https://cloud.2smart.com/robot/v1`
- **Official documentation:** [Create dashboard](https://cloud.2smart.com/swagger/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Dashboard title |
| `schema` | body | `string` | yes | Schema JSON string |
| `device_id` | body | `string` | no | Optional: id of device taken from product |
| `version` | body | `string` | no | Optional: Initial version (0.0.1 by default) |
