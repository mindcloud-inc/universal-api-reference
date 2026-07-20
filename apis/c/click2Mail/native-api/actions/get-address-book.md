# Get Address Book with Click2Mail

Retrieves an address book from Click2Mail.

## Endpoint

- **Method:** `GET`
- **Path:** `/molpro/addressBook/{id}`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Get Address Book](https://developers.click2mail.com/reference/getaddressdetails)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Address book id |
| `offset` | query | `number` | no | Offset for the next set of addresses |
| `limit` | query | `number` | no | number of addresses to be retrieve for address book. |
