# List Custom Fields with Kit

Lists custom fields in your Kit account.

## Endpoint

- **Method:** `GET`
- **Path:** `/custom_fields`
- **Base URL:** `https://api.kit.com/v4`
- **Official documentation:** [List Custom Fields](https://developers.kit.com/api-reference/custom-fields/list-custom-fields)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_total_count` | query | `boolean` | no | Set to true to include total_count in the response. Kit notes this can make the request slower. |
