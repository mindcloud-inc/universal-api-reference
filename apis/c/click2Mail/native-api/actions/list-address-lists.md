# List Address Lists with Click2Mail

Retrieves a list of address lists from Click2Mail.

## Endpoint

- **Method:** `GET`
- **Path:** `/molpro/addressLists`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [List Address Lists](https://developers.click2mail.com/reference/getaddresslist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numberOfLists` | query | `number` | no | number of lists to return |
| `offset` | query | `number` | no | offset from beginning to allow you to paginate through the lists |
| `searchkey` | query | `string` | no | return only lists where the list name contains the keyword |
| `count` | query | `string` | no | Returns a count of the number of lists in a customers account |
