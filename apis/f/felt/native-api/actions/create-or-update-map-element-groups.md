# Create Or Update Map Element Groups with Felt

Creates or updates map element groups in Felt.

## Endpoint

- **Method:** `POST`
- **Path:** `/maps/:mapId/element_groups`
- **Base URL:** `https://felt.com/api/v2`
- **Official documentation:** [Create Or Update Map Element Groups](https://developers.felt.com/rest-api/api-reference/elements)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `mapId` | path | `string` | yes | The ID of the map to create the group in. |
| `elementGroups[]` | body | `array<object>` | yes | Element groups to create or update. |
