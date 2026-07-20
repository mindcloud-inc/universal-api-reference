# List Lists with BigMailer

Retrieves lists from a BigMailer brand.

## Endpoint

- **Method:** `GET`
- **Path:** `/brands/:brand_id/lists`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [List Lists](https://docs.bigmailer.io/reference/listlists)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand whose lists should be returned. |
