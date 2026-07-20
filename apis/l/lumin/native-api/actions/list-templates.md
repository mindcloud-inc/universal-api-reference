# List Templates with Lumin

## Endpoint

- **Method:** `GET`
- **Path:** `/templates`
- **Base URL:** `https://api.luminpdf.com/v1`
- **Official documentation:** [List Templates](https://developers.luminpdf.com/api/list-templates/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Which page of templates to return. |
| `limit` | query | `number` | no | How many templates to return. One of 10, 25, or 50. |
