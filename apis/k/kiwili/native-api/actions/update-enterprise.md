# Update Enterprise with Kiwili

Updates an existing enterprise in Kiwili.

## Endpoint

- **Method:** `PUT`
- **Path:** `/enterprise/:enterprise_id`
- **Base URL:** `https://mindcloud.kiwili.com/api`
- **Official documentation:** [Update Enterprise](https://api.kiwili.com/api/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `enterprise_id` | path | `number` | yes | The Kiwili enterprise ID to update. |
| `IsClient` | body | `boolean` | no | Whether the enterprise is a client. |
| `Name` | body | `string` | no | The updated enterprise name. |
