# Add Addresses From Address Book with Click2Mail

Adds address book addresses to a Click2Mail address list.

## Endpoint

- **Method:** `POST`
- **Path:** `/molpro/addressLists/address/addressBook`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Add Addresses From Address Book](https://developers.click2mail.com/reference/addaddressesfromaddressbook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `object` | yes | array of address ids |
| `baseAddressListId` | query | `number` | no | List ID to upadate |
| `jobAddressListId` | query | `number` | no | List ID to upadate |
