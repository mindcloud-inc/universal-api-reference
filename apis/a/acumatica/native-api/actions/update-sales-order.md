# Update Sales Order with Acumatica

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/{endpointName}/{endpointVersion}/SalesOrder`
- **Base URL:** `{uRL}`
- **Official documentation:** [Update Sales Order](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderNbr` | body | `object` | no |
| `orderNbr.value` | body | `string` | no |
| `orderType.value` | body | `string` | no |
| `usrLogShipID.value` | body | `string` | no |
| `usrLogShipID` | body | `object` | no |
| `orderType` | body | `object` | no |
