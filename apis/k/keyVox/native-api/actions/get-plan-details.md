# Get Plan Details with KeyVox

Retrieves room plan details from KeyVox.

## Endpoint

- **Method:** `POST`
- **Path:** `/plan/detail`
- **Base URL:** `https://eco.blockchainlock.io/api/eagle-pms`
- **Official documentation:** [Get Plan Details](https://developers.keyvox.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `commodityId` | body | `string` | no | 部屋プランID |
| `placeId` | body | `string` | no | 場所ID |
| `targetType` | body | `string` | no | プランタイプ<br>"order":予約<br>"order"で指定された場合、「貸出不可時間」を返却する |
