# List Models with ImageRouter

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/models`
- **Base URL:** `https://api.imagerouter.io`
- **Official documentation:** [List Models](https://docs.imagerouter.io/api-reference/models/)

## Capabilities

This operation supports [filtering](../README.md#filtering) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `outputType` | query | `string` | no | Filter by output type: image or video. |
| `inputType` | query | `string` | no | Filter by supported input: image, mask, quality, size, or seconds. |
| `provider` | query | `string` | no | Filter by provider name, partial and case-insensitive. |
| `name` | query | `string` | no | Filter by model name or alias, partial and case-insensitive. |
| `free` | query | `boolean` | no | true to show only free models, false to show only paid models. |
| `fields` | query | `string` | no | Comma-separated response fields to include; id is always included. |
| `sort` | query | `string` | no | Sort by name, provider, price, or date. |
| `limit` | query | `number` | no | Maximum number of models to return. |
