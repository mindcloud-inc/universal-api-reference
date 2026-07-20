# List Templates with Bannerbear

Retrieves templates from Bannerbear.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/templates`
- **Base URL:** `https://api.bannerbear.com`
- **Official documentation:** [List Templates](https://developers.bannerbear.com/v2/#list-all-templates)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | Filter templates by name. |
| `tag` | query | `string` | no | Filter templates by tag. |
| `extended` | query | `boolean` | no | Return the extended template response. |
