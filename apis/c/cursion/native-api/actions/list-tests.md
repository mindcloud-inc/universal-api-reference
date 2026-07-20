# List Tests with Cursion

Retrieves a list of tests from Cursion.

## Endpoint

- **Method:** `GET`
- **Path:** `/test`
- **Base URL:** `https://api.cursion.dev/v1/ops`
- **Official documentation:** [List Tests](https://docs.cursion.dev/api/test)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_id` | query | `string` | yes | The page ID to list tests for. |
