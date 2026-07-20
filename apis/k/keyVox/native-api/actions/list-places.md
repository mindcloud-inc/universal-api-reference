# List Places with KeyVox

Lists places in your KeyVox account.

## Endpoint

- **Method:** `POST`
- **Path:** `/place/list`
- **Base URL:** `https://eco.blockchainlock.io/api/eagle-pms`
- **Official documentation:** [List Places](https://developers.keyvox.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | body | `string` | no | １ページ件数 |
| `page` | body | `string` | no | ページ番号 |
| `placeType` | body | `string` | no | 場所カテゴリ<br>"hotel":ビルディング, "locker":ロッカー, "doubleLocker":両面開きロッカー, "vendingMachine":自動販売機 |
