# Create Connection with Pabbly Hook

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/connections`
- **Base URL:** `https://hook.pabbly.com`
- **Official documentation:** [Create Connection](https://apidocs.pabbly.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Connection name. |
| `folder_id` | body | `string` | yes | Folder ID for the connection. |
| `source` | body | `object` | yes | Source configuration object. |
| `destination` | body | `object` | yes | Destination configuration object. |
| `retry` | body | `object` | no | Retry configuration object. |
| `delay` | body | `object` | no | Delay configuration object. |
| `trs_id` | body | `string` | no | Transformation ID to apply. |
| `filter` | body | `object` | no | Connection filter configuration object. |
