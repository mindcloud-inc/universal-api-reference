# List Quicksend Templates with AMcards.com

Retrieves Quicksend templates from your AMcards.com account.

## Endpoint

- **Method:** `GET`
- **Path:** `/quicksendtemplate/`
- **Base URL:** `https://amcards.com/.api/v1`
- **Official documentation:** [List Quicksend Templates](https://staging.amcards.com/docs/developers-only/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name__icontains` | query | `string` | no | Filter quicksend templates by partial name match. |
