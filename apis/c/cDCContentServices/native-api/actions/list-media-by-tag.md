# List Media By Tag with CDC Content Services

Retrieves media by tag from CDC Content Services.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/resources/tags/[:tagId]/media`
- **Base URL:** `https://tools.cdc.gov/api`
- **Official documentation:** [List Media By Tag](https://tools.cdc.gov/api/docs/info.aspx)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tagId` | path | `number` | yes | CDC tag identifier. |
