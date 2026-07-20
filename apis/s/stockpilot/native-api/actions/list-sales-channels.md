# List Sales Channels with Stockpilot

Retrieves sales channels from Stockpilot.

## Endpoint

- **Method:** `GET`
- **Path:** `/sales-channels`
- **Base URL:** `https://api.stockpilot.dev`
- **Official documentation:** [List Sales Channels](https://api.stockpilot.dev/redoc#operation/get_channels_sales_channels_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | query | `number` | no | Page number for pagination |
| `page_size` | query | `number` | no | Number of items per page |
