# Get Address List Info with Click2Mail

Retrieves address list metadata from Click2Mail.

## Endpoint

- **Method:** `GET`
- **Path:** `/molpro/addressLists/info`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Get Address List Info](https://developers.click2mail.com/reference/getaddresslistinfo)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addressType` | query | `string` | no | Use for filtering addresses. |
| `baseAddressListId` | query | `number` | no | Require when other parameter jobAddressListId is null. |
| `jobAddressListId` | query | `number` | no | Require when other parameter baseAddressListId is null. |
| `offset` | query | `number` | no | Use for filtering addresses. |
| `limit` | query | `number` | no | Integer referring number of addresses to be return. Default is 10. |
