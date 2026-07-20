# List Templates with BigMailer

Retrieves templates from a BigMailer brand.

## Endpoint

- **Method:** `GET`
- **Path:** `/brands/:brand_id/templates`
- **Base URL:** `https://api.bigmailer.io/v1`
- **Official documentation:** [List Templates](https://docs.bigmailer.io/reference/listtemplates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `brand_id` | path | `string` | yes | ID of the brand whose templates should be returned. |
