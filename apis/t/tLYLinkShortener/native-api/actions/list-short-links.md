# List Short Links with TLY Link Shortener

Retrieves short links from TLY Link Shortener.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/link/list`
- **Base URL:** `https://api.t.ly`
- **Official documentation:** [List Short Links](https://t.ly/docs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search short links by text. |
| `tag_ids[]` | query | `array<number>` | no | Return links associated with the specified tag IDs. |
| `pixel_ids[]` | query | `array<number>` | no | Return links associated with the specified pixel IDs. |
| `start_date` | query | `date` | no | Filter links created on or after this date. |
| `end_date` | query | `date` | no | Filter links created on or before this date. |
| `domains[]` | query | `array<number>` | no | Return links associated with the specified custom domain IDs. |
