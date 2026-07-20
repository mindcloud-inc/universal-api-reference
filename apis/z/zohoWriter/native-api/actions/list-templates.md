# List Templates with Zoho Writer

Retrieves templates from Zoho Writer.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/templates`
- **Base URL:** `{api_domain}/writer/api`
- **Official documentation:** [List Templates](https://www.zoho.com/writer/help/api/v1/get-list-of-templates.html)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Template scope to list: personal or organization. |
