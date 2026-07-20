# List Adjacent Entities with OpenSanctions

## Endpoint

- **Method:** `GET`
- **Path:** `/entities/:entity_id/adjacent`
- **Base URL:** `https://api.opensanctions.org`
- **Official documentation:** [List Adjacent Entities](https://api.opensanctions.org/docs#/Data%20access/Fetch_Adjacent_Entities__entities__entity_id__adjacent_get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_id` | path | `string` | yes | ID of the entity whose graph context is requested. |
