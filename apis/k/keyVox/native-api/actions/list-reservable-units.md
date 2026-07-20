# List Reservable Units with KeyVox

Lists doors in your KeyVox account.

## Endpoint

- **Method:** `POST`
- **Path:** `/unit/list`
- **Base URL:** `https://eco.blockchainlock.io/api/eagle-pms`
- **Official documentation:** [List Reservable Units](https://developers.keyvox.co/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `count` | body | `string` | no | １ページ件数 |
| `page` | body | `string` | no | ページ番号 |
| `placeId` | body | `string` | no | 場所ID |
| `searchWord` | body | `string` | no | 検索キーワード |
| `unitBusinessType` | body | `string` | no | ビジネスタイプ<br>"housing":宿泊, "rentalSpace":レンタルスペース, "conferenceRoom":コーワーキング, "locker":ロッカー, "airdrop":ドロップイン, "vendingMachine":自動販売機 |
