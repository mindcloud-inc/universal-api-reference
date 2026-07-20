# List Public Templates with AMcards.com

Retrieves public card templates from AMcards.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/publictemplate/`
- **Base URL:** `https://amcards.com/.api/v1`
- **Official documentation:** [List Public Templates](https://staging.amcards.com/docs/developers-only/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category__id` | query | `number` | no | Filter public templates by category ID. |
| `name__icontains` | query | `string` | no | Filter public templates whose name contains the given text. |
