# List Fields with BigMailer

Retrieves fields from a BigMailer brand.

## Endpoint

- **Method:** `GET`
- **Path:** `/brands/:brand_id/fields`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [List Fields](https://docs.bigmailer.io/reference/listfields)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand whose fields should be returned. |
