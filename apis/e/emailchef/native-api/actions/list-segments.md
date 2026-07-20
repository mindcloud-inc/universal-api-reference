# List Segments with Emailchef

Retrieves segments for a list from Emailchef.

## Endpoint

- **Method:** `GET`
- **Path:** `lists/:list_id/segments`
- **Base URL:** `https://app.emailchef.com/apps/api/v1`
- **Official documentation:** [List Segments](https://emailchef.com/integration/#/Segments/getSegments)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | path | `string` | yes | The Emailchef list ID. |
