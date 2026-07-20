# List Tags with Front

Retrieves a list of tags from Front.

## Endpoint

- **Method:** `GET`
- **Path:** `/tags`
- **Base URL:** `https://api2.frontapp.com`
- **Official documentation:** [List Tags](https://dev.frontapp.com/reference/list-tags)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort_by` | query | `list` | no | Field used to sort the tags. Front only documents id. Accepted values: `0`. |
| `sort_order` | query | `list` | no | Order by which results should be sorted. Accepted values: `0`, `1`. |
