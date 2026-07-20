# Add Address List Addresses with Click2Mail

Adds addresses to a Click2Mail address list.

## Endpoint

- **Method:** `POST`
- **Path:** `/molpro/addressLists/address2`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Add Address List Addresses](https://developers.click2mail.com/reference/addaddresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseAddressListId` | query | `number` | no | Require when other parameter jobAddressListId is null. |
| `jobAddressListId` | query | `number` | no | Require when other parameter baseAddressListId is null. |
| `addresses` | body | `object` | no | — |
| `addressListName` | body | `string` | no | — |
| `addressMappingId` | body | `string` | no | — |
