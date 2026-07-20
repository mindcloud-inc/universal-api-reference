# List Groups with AMcards.com

Retrieves your contact groups from AMcards.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/group/`
- **Base URL:** `https://amcards.com/.api/v1`
- **Official documentation:** [List Groups](https://staging.amcards.com/docs/developers-only/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name__icontains` | query | `string` | no | Filter groups by partial name match. |
