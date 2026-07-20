# Update Group with MoreApp

Updates a group in MoreApp.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v2/customers/{{customerId}}/groups/{{groupId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Update Group](https://docs.moreapp.com/docs/developer-docs/dd580afded7b4-modify-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `groupId` | path | `string` | yes | MoreApp group identifier. |
| `name` | body | `string` | yes | Updated group name. |
