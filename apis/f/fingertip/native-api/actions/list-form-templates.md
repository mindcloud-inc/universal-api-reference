# List Form Templates with Fingertip

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/form-templates`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [List Form Templates](https://docs.fingertip.com/openapi-specs/list-form-templates.md)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | query | `string` | yes | ID of the site to list form templates for. |
| `search` | query | `string` | no | Optional search query. |
