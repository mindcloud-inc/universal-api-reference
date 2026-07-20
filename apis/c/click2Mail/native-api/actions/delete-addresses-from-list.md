# Delete Addresses From List with Click2Mail

Deletes addresses from a Click2Mail list.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/molpro/addressLists`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Delete Addresses From List](https://developers.click2mail.com/reference/deleteaddresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addressType` | query | `string` | no | Use for filtering addresses. |
| `baseAddressListId` | query | `number` | no | Require when other parameter jobAddressListId is null. |
| `jobAddressListId` | query | `number` | no | Require when other parameter baseAddressListId is null. |
| `id[]` | query | `array<number>` | no | Require when other parameter addressType is null. Identify addresses to be deleted. |
