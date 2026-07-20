# List Topics with CDC Content Services

Retrieves topics from CDC Content Services.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/resources/topics`
- **Base URL:** `https://tools.cdc.gov/api`
- **Official documentation:** [List Topics](https://tools.cdc.gov/api/docs/info.aspx)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `showChild` | query | `boolean` | no | Return sub-topics in the items attribute when true. |
| `language` | query | `string` | no | Filter topics by language. CDC defaults to English when omitted. |
| `mediaType` | query | `string` | no | Filter topics using a CDC media type. |
