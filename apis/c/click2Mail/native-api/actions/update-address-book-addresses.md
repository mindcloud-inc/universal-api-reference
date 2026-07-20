# Update Address Book Addresses with Click2Mail

Updates addresses in a Click2Mail address book.

## Endpoint

- **Method:** `PUT`
- **Path:** `/molpro/addressBook/{id}/address`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Update Address Book Addresses](https://developers.click2mail.com/reference/updateaddresses_1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Address Book id |
| `addresses` | body | `object` | no | — |
| `addressListName` | body | `string` | no | — |
| `addressMappingId` | body | `string` | no | — |
