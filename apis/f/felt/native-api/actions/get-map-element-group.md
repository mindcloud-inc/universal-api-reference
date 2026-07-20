# Get Map Element Group with Felt

Retrieves a map element group from Felt.

## Endpoint

- **Method:** `GET`
- **Path:** `/maps/:mapId/element_groups/:groupId`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Get Map Element Group](https://developers.felt.com/rest-api/api-reference/elements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The ID of the map. |
| `groupId` | path | `string` | yes | The ID of the element group. |
