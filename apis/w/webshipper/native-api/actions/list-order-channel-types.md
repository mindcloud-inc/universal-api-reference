# List Order Channel Types with Webshipper

Retrieves order channel types from Webshipper.

## Endpoint

- **Method:** `GET`
- **Path:** `/order_channel_types`
- **Base URL:** `https://{accountName}.api.webshipper.io/v2`
- **Official documentation:** [List Order Channel Types](https://docs.webshipper.io/#order_channel_types)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filter[id]` | query | `string` | no | Filter by id. |
| `filter[by_name]` | query | `string` | no | Filter by name. |
