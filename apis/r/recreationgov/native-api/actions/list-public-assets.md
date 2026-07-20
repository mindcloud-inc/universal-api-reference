# List Public Assets with Recreation.gov

## Endpoint

- **Method:** `GET`
- **Path:** `/public/assets`
- **Base URL:** `https://ridb.recreation.gov/api/v1`
- **Official documentation:** [List Public Assets](https://ridb.recreation.gov/shared/swagger/ridb.yaml)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assetTypes[]` | query | `array<string>` | no | Send multiple values as a array. |
| `orgIds[]` | query | `array<number>` | no | Send multiple values as a array. |
| `activity` | query | `string` | no | — |
| `state` | query | `string` | no | — |
| `terms` | query | `string` | no | — |
| `limit` | query | `number` | no | — |
| `offset` | query | `number` | no | — |
| `sort` | query | `string` | no | — |
