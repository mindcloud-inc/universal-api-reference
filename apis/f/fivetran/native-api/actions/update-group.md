# Update Group with Fivetran

Updates an existing group in your Fivetran account.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/groups/[:groupId]`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Update Group](https://fivetran.com/docs/rest-api/api-reference/group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier for the group within Fivetran. |
| `name` | body | `string` | no | The updated name of the group within your account. |
