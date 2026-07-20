# Get Group with Fivetran

Retrieves a group from your Fivetran account.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/[:groupId]`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Get Group](https://fivetran.com/docs/rest-api/api-reference/group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier for the group within Fivetran. |
