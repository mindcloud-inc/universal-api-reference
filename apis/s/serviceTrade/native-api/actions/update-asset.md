# Update Asset with ServiceTrade

Updates an existing asset in ServiceTrade.

## Endpoint

- **Method:** `PUT`
- **Path:** `asset/:assetId`
- **Base URL:** `https://api.servicetrade.com/api`
- **Official documentation:** [Update Asset](https://api.servicetrade.com/api/docs#resource-asset)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `assetId` | path | `number` | yes | Asset to update. |
| `properties.notes` | body | `string` | no | Updated notes for asset definitions that support it. |
| `taskListId` | body | `number` | no | Updated task list for the asset. |
