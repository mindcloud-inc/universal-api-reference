# Release Purchase Receipt with Acumatica

## Endpoint

- **Method:** `POST`
- **Path:** `/entity/{endpointName}/{endpointVersion}/PurchaseReceipt/ReleasePurchaseReceipt`
- **Base URL:** `{uRL}`
- **Official documentation:** [Release Purchase Receipt](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `entity.ReceiptNbr.value` | body | `string` | no |
| `entity` | body | `object` | no |
| `entity.id` | body | `string` | no |
| `entity.ReceiptNbr` | body | `object` | no |
