# List Asset Infos with ThingsBoard

Retrieves asset info records from ThingsBoard.

## Endpoint

- **Method:** `GET`
- **Path:** `/assetInfos/all`
- **Base URL:** `{baseUrl}/api`
- **Official documentation:** [List Asset Infos](https://thingsboard.cloud/swagger-ui/index.html#/asset-controller/getAllAssetInfos)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageSize` | query | `number` | yes | Maximum number of asset info records to return in one page. |
| `page` | query | `number` | yes | Zero-based page number. |
