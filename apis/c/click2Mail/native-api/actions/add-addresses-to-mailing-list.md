# Add Addresses To Mailing List with Click2Mail

Adds addresses to a Click2Mail mailing list.

## Endpoint

- **Method:** `POST`
- **Path:** `/molpro/addressLists/address`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Add Addresses To Mailing List](https://developers.click2mail.com/reference/addaddressestomaillist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `object` | yes | array of address ids |
| `name` | query | `string` | no | new list name |
