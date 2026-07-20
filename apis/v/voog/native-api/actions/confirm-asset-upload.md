# Confirm Asset Upload with Voog

Confirms an asset upload in the current Voog site.

## Endpoint

- **Method:** `PUT`
- **Path:** `/assets/:assetId/confirm`
- **Base URL:** `{siteUrl}/admin/api`
- **Official documentation:** [Confirm Asset Upload](https://www.voog.com/developers/api/resources/assets)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assetId` | path | `number` | yes | Numeric asset ID. |
