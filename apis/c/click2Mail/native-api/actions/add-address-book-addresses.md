# Add Address Book Addresses with Click2Mail

Adds addresses to a Click2Mail address book.

## Endpoint

- **Method:** `POST`
- **Path:** `/molpro/addressBook/{id}/address`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Add Address Book Addresses](https://developers.click2mail.com/reference/addaddresses_1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Address Book id |
| `addresses` | body | `object` | no | — |
| `addressListName` | body | `string` | no | — |
| `addressMappingId` | body | `string` | no | — |
