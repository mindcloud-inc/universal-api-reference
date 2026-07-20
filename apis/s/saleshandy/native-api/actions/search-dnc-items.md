# Search DNC Items with Saleshandy

## Endpoint

- **Method:** `GET`
- **Path:** `/dnc/item/search`
- **Base URL:** `https://open-api.saleshandy.com/v1`
- **Official documentation:** [Search DNC Items](https://developer.saleshandy.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Optional DNC item search string. |
| `type` | query | `string` | yes | DNC item type to search for. |
