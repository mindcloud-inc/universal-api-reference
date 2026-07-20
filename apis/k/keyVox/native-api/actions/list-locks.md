# List Locks with KeyVox

Lists locks in your KeyVox account.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/getLocks`
- **Base URL:** `https://eco.blockchainlock.io/api/eagle-pms`
- **Official documentation:** [List Locks](https://developers.keyvox.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page` | body | `number` | no | 1ページ目から指定 |
| `count` | body | `number` | no | 表示件数（最大100前後） |
