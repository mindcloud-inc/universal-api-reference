# List Templates with AMcards.com

Retrieves template records from your AMcards.com account.

## Endpoint

- **Method:** `GET`
- **Path:** `/template/`
- **Base URL:** `https://amcards.com/.api/v1`
- **Official documentation:** [List Templates](https://staging.amcards.com/docs/developers-only/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name__icontains` | query | `string` | no | Filter templates by partial name match. |
