# Create API Key with MindCloud

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/api-keys`
- **Base URL:** `https://connect.mindcloud.co`
- **Official documentation:** [Create API Key](https://connect.mindcloud.co/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accessLevel` | body | `string` | no | Access Level for this MindCloud v2 request. |
| `name` | body | `string` | yes | Name for this MindCloud v2 request. |
