# List Visitors with Weberlo

Retrieves a list of visitors from Weberlo.

## Endpoint

- **Method:** `POST`
- **Path:** `/visitor/list`
- **Base URL:** `https://connect.weberlo.com`
- **Official documentation:** [List Visitors](https://developers.weberlo.com/#tag/Visitor/paths/~1visitor~1list/post)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `start_date` | body | `string` | yes | Start of the visitor search window. |
| `end_date` | body | `string` | yes | End of the visitor search window. |
