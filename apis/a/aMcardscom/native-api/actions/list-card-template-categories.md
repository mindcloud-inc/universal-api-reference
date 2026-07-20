# List Card Template Categories with AMcards.com

Retrieves card template categories from AMcards.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/category/`
- **Base URL:** `https://amcards.com/.api/v1`
- **Official documentation:** [List Card Template Categories](https://staging.amcards.com/docs/developers-only/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parent__id` | query | `number` | no | Filter categories by parent category ID. |
| `parent__title__icontains` | query | `string` | no | Filter categories by partial parent-title match. |
| `title__icontains` | query | `string` | no | Filter categories by partial title match. |
