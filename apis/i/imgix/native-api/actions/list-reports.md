# List Reports with imgix

Retrieves reports from imgix.

## Endpoint

- **Method:** `GET`
- **Path:** `reports`
- **Base URL:** `https://api.imgix.com/api/v1`
- **Official documentation:** [List Reports](https://docs.imgix.com/en-US/apis/management/reports)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page[number]` | query | `number` | no | Zero-indexed page number for report lists. |
| `page[size]` | query | `number` | no | Page size for report lists. |
