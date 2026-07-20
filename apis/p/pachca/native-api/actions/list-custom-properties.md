# List custom properties with Pachca

## Endpoint

- **Method:** `GET`
- **Path:** `/custom_properties`
- **Base URL:** `https://api.pachca.com/api/shared/v1`
- **Official documentation:** [List custom properties](https://dev.pachca.com/reference/custom-properties)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entity_type` | query | `string` | yes | Entity type to list custom properties for, such as User or Task. |
