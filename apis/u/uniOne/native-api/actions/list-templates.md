# List Templates with UniOne

Retrieves email templates from UniOne, optionally by name.

## Endpoint

- **Method:** `POST`
- **Path:** `template/list.json`
- **Base URL:** `https://api.unione.io/en/transactional/api/v1`
- **Official documentation:** [List Templates](https://docs.unione.io/en/web-api-ref#template-list)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Optional exact template name filter. |
