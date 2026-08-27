# Purchase Receipt with Acumatica

## Endpoint

- **Method:** `PUT`
- **Path:** `/entity/{endpointName}/{endpointVersion}/PurchaseReceipt`
- **Base URL:** `{uRL}`
- **Official documentation:** [Purchase Receipt](https://help.acumatica.com/(W(5))/Help?ScreenId=ShowWiki&pageid=56831ee7-14b0-45ef-8207-dace30beb2cb)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `Branch.value` | body | `string` | no |
| `Date.value` | body | `string` | no |
| `Details[].ExpirationDate.value` | body | `string` | no |
| `Details[].LineNbr.value` | body | `number` | no |
| `Details[].Location.value` | body | `string` | no |
| `Details[].LotSerialNbr.value` | body | `string` | no |
| `Details[].Note.value` | body | `string` | no |
| `Details[].POLineNbr.value` | body | `number` | no |
| `Details[].POOrderNbr.value` | body | `string` | no |
| `Details[].POOrderType.value` | body | `string` | no |
| `Details[].ReceiptQty` | body | `object` | no |
| `Details[].ReceiptQty.value` | body | `number` | no |
| `Details[].UsrLogTranID.value` | body | `string` | no |
| `Details[].UsrLPNbr.value` | body | `string` | no |
| `Hold.value` | body | `boolean` | no |
| `Location.value` | body | `string` | no |
| `Note.value` | body | `string` | no |
| `ReceiptNbr.value` | body | `string` | no |
| `Type.value` | body | `string` | no |
| `UsrLogReceiptID.value` | body | `string` | no |
| `UsrLogReceived.value` | body | `boolean` | no |
| `VendorID.value` | body | `string` | no |
| `Details[].POOrderType` | body | `object` | no |
| `Type` | body | `object` | no |
| `Details[].POOrderNbr` | body | `object` | no |
| `Hold` | body | `object` | no |
| `Date` | body | `object` | no |
| `Details[].POLineNbr` | body | `object` | no |
| `Details[].LotSerialNbr` | body | `object` | no |
| `VendorID` | body | `object` | no |
| `Details[].ExpirationDate` | body | `object` | no |
| `Location` | body | `object` | no |
| `Branch` | body | `object` | no |
| `Details[].UsrLPNbr` | body | `object` | no |
| `Details[].UsrLogTranID` | body | `object` | no |
| `Note` | body | `object` | no |
| `Details[]` | body | `array` | no |
| `Details[].Note` | body | `object` | no |
| `Details[].Location` | body | `object` | no |
| `UsrLogReceived` | body | `object` | no |
| `Details[].LineNbr` | body | `object` | no |
| `ReceiptNbr` | body | `object` | no |
| `UsrLogReceiptID` | body | `object` | no |
