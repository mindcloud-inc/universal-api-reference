# List Templates with Signaturit

Retrieves templates from Signaturit.

## Endpoint

- **Method:** `GET`
- **Path:** `/templates.json`
- **Base URL:** `https://api.sandbox.signaturit.com/v3`
- **API:** rest
- **Official documentation:** [List Templates](https://docs.signaturit.com/api/latest#templates_get_templates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of templates to return. |
| `offset` | query | `number` | no | Results offset. |
