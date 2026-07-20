# List Scans with Cursion

Retrieves a list of scans from Cursion.

## Endpoint

- **Method:** `GET`
- **Path:** `/scan`
- **Base URL:** `https://api.cursion.dev/v1/ops`
- **Official documentation:** [List Scans](https://docs.cursion.dev/api/scan)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_id` | query | `string` | yes | The page ID to list scans for. |
