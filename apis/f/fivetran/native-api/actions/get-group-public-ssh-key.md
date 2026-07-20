# Get Group Public SSH Key with Fivetran

Retrieves a group's public SSH key from Fivetran.

## Endpoint

- **Method:** `GET`
- **Path:** `/groups/[:groupId]/public-key`
- **Base URL:** `https://api.fivetran.com/v1`
- **Official documentation:** [Get Group Public SSH Key](https://fivetran.com/docs/rest-api/api-reference/group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupId` | path | `string` | yes | The unique identifier for the group within Fivetran. |
