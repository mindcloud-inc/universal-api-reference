# Update Company with MindCloud

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/companies/:companyId`
- **Base URL:** `https://connect.mindcloud.co`
- **Official documentation:** [Update Company](https://connect.mindcloud.co/v2/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `companyId` | path | `string` | yes | Company ID for this MindCloud v2 request. |
| `description` | body | `string` | no | Description for this MindCloud v2 request. |
| `name` | body | `string` | no | Name for this MindCloud v2 request. |
| `timezone` | body | `string` | no | Timezone for this MindCloud v2 request. |
