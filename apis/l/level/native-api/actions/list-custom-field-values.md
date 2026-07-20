# List Custom Field Values with Level

Retrieves custom field values from Level.

## Endpoint

- **Method:** `GET`
- **Path:** `/custom_field_values`
- **Base URL:** `https://api.level.io/v2`
- **Official documentation:** [List Custom Field Values](https://levelapi.readme.io/reference/custom-field-values)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assigned_to_id` | query | `string` | no | Filter to only include values assigned to the specified group or device. |
| `custom_field_id` | query | `string` | no | Filter to only include values for the specified custom field. |
