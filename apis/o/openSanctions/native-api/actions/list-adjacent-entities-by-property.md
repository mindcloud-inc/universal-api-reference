# List Adjacent Entities By Property with OpenSanctions

## Endpoint

- **Method:** `GET`
- **Path:** `/entities/:entity_id/adjacent/:property_name`
- **Base URL:** `https://api.opensanctions.org`
- **Official documentation:** [List Adjacent Entities By Property](https://api.opensanctions.org/docs#/Data%20access/Fetch_Adjacent_by_Property__entities__entity_id__adjacent__property_name__get)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_id` | path | `string` | yes | ID of the entity whose graph context is requested. |
| `property_name` | path | `string` | yes | Adjacent relationship or property group to fetch for the entity. |
