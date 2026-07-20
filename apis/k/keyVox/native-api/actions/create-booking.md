# Create Booking with KeyVox

Creates a new booking in KeyVox.

## Endpoint

- **Method:** `POST`
- **Path:** `/bacsorder/create`
- **Base URL:** `https://eco.blockchainlock.io/api/eagle-pms`
- **Official documentation:** [Create Booking](https://developers.keyvox.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channelOrderNo` | body | `string` | no | 予約サイト予約番号 |
| `checkin` | body | `string` | no | チェックイン時間<br>UNIX時間（秒）で指定します |
| `checkout` | body | `string` | no | チェックアウト時間<br>UNIX時間（秒）で指定します |
| `contactAddress` | body | `string` | no | お客様住所 |
| `contactCertificateNum` | body | `string` | no | お客様証明書ID |
| `orderContact` | body | `string` | no | お客様氏名 |
| `orderSource` | body | `string` | no | 予約サイト名(システム名) |
| `placeId` | body | `string` | no | 場所ID |
| `userId` | body | `string` | no | ユーザーID |
