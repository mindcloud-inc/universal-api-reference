# Update Sales Receipt with QuickBooks Online

## Endpoint

- **Method:** `POST`
- **Path:** `/salesreceipt`
- **Base URL:** `https://:quickbooksEnvironment/v3/company/:realmId`
- **Official documentation:** [Update Sales Receipt](https://developer.intuit.com/app/developer/qbo/docs/api/accounting/all-entities/purchaseorder#create-a-purchaseorder)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `CustomField[].NumberValue` | body | `number` | no |
| `SyncToken` | body | `string` | no |
| `Id` | body | `string` | no |
| `sparse` | body | `boolean` | no |
| `minorversion` | query | `string` | no |
| `TrackingNum` | body | `string` | no |
| `include` | query | `string` | no |
| `CustomField[]` | body | `array` | no |
