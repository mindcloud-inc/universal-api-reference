# List Sources with imgix

Retrieves sources from imgix.

## Endpoint

- **Method:** `GET`
- **Path:** `sources`
- **Base URL:** `https://api.imgix.com/api/v1`
- **Official documentation:** [List Sources](https://docs.imgix.com/en-US/apis/management/sources)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page[number]` | query | `number` | no | Zero-indexed page number for source lists. |
| `page[size]` | query | `number` | no | Page size for source lists. |
