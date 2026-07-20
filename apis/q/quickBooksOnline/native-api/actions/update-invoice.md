# Update Invoice with QuickBooks Online

## Endpoint

- **Method:** `POST`
- **Path:** `/invoice`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [Update Invoice](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/invoice#create-an-invoice)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Id` | body | `string` | no | — |
| `CustomField[].NumberValue` | body | `number` | no | — |
| `Line[0].SalesItemLineDetail.ItemRef.value` | body | `string` | no | Item ID to bill on the first invoice line. |
| `SyncToken` | body | `string` | no | — |
| `CustomField[]` | body | `array` | no | — |
| `Line[]` | body | `array` | no | — |
| `CustomerRef` | body | `object` | no | — |
| `TrackingNum` | body | `string` | no | — |
