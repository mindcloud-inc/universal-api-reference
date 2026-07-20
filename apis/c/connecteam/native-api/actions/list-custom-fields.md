# List Custom Fields with Connecteam

Retrieves all custom fields associated with the account. Optionally, filter the results by categories, names, types, or custom field IDs.

## Endpoint

- **Method:** `GET`
- **Path:** `/users/v1/custom-fields`
- **Base URL:** `https://api.connecteam.com`
- **Official documentation:** [List Custom Fields](https://developer.connecteam.com/reference/get_custom_fields_users_v1_custom_fields_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customFieldIds` | query | `array<number>` | no | Send multiple values as a array. |
| `categoryIds` | query | `array<number>` | no | Send multiple values as a array. |
| `customFieldTypes` | query | `array<string>` | no | Send multiple values as a array. |
| `customFieldNames` | query | `array<string>` | no | Send multiple values as a array. |
| `limit` | query | `number` | no | — |
| `offset` | query | `number` | no | — |
| `sort` | query | `string` | no | — |
| `order` | query | `string` | no | — |
