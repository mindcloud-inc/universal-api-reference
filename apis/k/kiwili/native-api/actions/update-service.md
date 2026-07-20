# Update Service with Kiwili

Updates an existing service in Kiwili.

## Endpoint

- **Method:** `PUT`
- **Path:** `/service/:service_id`
- **Base URL:** `https://mindcloud.kiwili.com/api`
- **Official documentation:** [Update Service](https://api.kiwili.com/api/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Active` | body | `boolean` | no | Whether the service is active. |
| `Billable` | body | `boolean` | no | Whether the service is billable. |
| `Name` | body | `string` | no | The updated service name. |
| `Rate` | body | `number` | no | The updated service rate. |
| `service_id` | path | `number` | yes | The Kiwili service ID to update. |
