# List Booking Orders with KeyVox

Lists booking orders in your KeyVox account.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/getBookingOrders`
- **Base URL:** `https://eco.blockchainlock.io/api/eagle-pms`
- **Official documentation:** [List Booking Orders](https://developers.keyvox.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `unitId` | body | `string` | no | WEB管理画面「BACS」で設定したドア(部屋)ごとに割り当てられるユニークIDです。getUnitsで取得可能です |
