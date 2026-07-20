# Check Address List Name with Click2Mail

Checks whether an address list name is available in Click2Mail.

## Endpoint

- **Method:** `POST`
- **Path:** `/molpro/addressLists/checkName`
- **Base URL:** `https://stage-rest.click2mail.com`
- **Official documentation:** [Check Address List Name](https://developers.click2mail.com/reference/validateaddresslistname)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `addressListName` | query | `string` | yes | Address List name as it will be stored in your account |
