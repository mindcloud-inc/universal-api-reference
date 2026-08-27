# Reopen Shipment with Acumatica

## Endpoint

- **Method:** `POST`
- **Path:** `/entity/{endpointName}/{endpointVersion}/SalesOrder/ReopenSalesOrder`
- **Base URL:** `{uRL}`
- **Official documentation:** [Reopen Shipment](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entity.OrderNbr.value` | body | `string` | no |
| `entity.OrderType.value` | body | `string` | no |
| `entity` | body | `object` | no |
| `entity.OrderType` | body | `object` | no |
| `entity.OrderNbr` | body | `object` | no |
