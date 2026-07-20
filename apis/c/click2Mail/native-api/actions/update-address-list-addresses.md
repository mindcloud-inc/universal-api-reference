# Update Address List Addresses with Click2Mail

Updates addresses in a Click2Mail address list.

## Endpoint

- **Method:** `PUT`
- **Path:** `/molpro/addressLists/address2`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Update Address List Addresses](https://developers.click2mail.com/reference/updateaddresses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `baseAddressListId` | query | `number` | no | Require when other parameter jobAddressListId is null. |
| `jobAddressListId` | query | `number` | no | Require when other parameter baseAddressListId is null. |
| `addresses` | body | `object` | no | — |
| `addressListName` | body | `string` | no | — |
| `addressMappingId` | body | `string` | no | — |
