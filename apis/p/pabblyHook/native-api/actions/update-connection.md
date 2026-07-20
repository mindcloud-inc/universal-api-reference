# Update Connection with Pabbly Hook

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v1/connections/:connectionId`
- **Base URL:** `https://hook.pabbly.com`
- **Official documentation:** [Update Connection](https://apidocs.pabbly.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connectionId` | path | `string` | yes | Connection ID to update. |
| `name` | body | `string` | no | Connection name. |
| `source` | body | `object` | yes | Source configuration object. |
| `destination` | body | `object` | yes | Destination configuration object. |
| `retry` | body | `object` | no | Retry configuration object. |
| `delay` | body | `object` | no | Delay configuration object. |
| `trs_id` | body | `string` | no | Transformation ID to apply. |
| `filter` | body | `object` | no | Connection filter configuration object. |
