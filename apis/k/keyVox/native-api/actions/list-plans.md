# List Plans with KeyVox

Lists room plans in your KeyVox account.

## Endpoint

- **Method:** `POST`
- **Path:** `/plan/list`
- **Base URL:** `https://eco.blockchainlock.io/api/eagle-pms`
- **Official documentation:** [List Plans](https://developers.keyvox.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | body | `string` | no | １ページ件数 |
| `page` | body | `string` | no | ページ番号 |
| `placeId` | body | `string` | no | 場所ID |
