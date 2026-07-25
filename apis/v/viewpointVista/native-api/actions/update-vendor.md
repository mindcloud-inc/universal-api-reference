# Update Vendor with Viewpoint Vista

## Endpoint

- **Method:** `POST`
- **Path:** `v1/direct/subscribers/:subscriber_code/vista/:api/2/data/vendors/actions/change`
- **Base URL:** `https://api.xchange.trimble.com/connect/`
- **API:** REST
- **Official documentation:** [Update Vendor](https://direct-api.xchange.trimble.com/reference/post-directsubscriberssubscriber_codevistaap2datavendorsactionschange)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `__key` | body | `object` | yes | "__key": {     "KeyID": 5   }, |
| `__key.KeyID` | body | `number` | no | — |
| `PaymentAddress.Address` | body | `string` | no | — |
| `APCo` | body | `number` | yes | — |
| `PaymentAddress.Address2` | body | `string` | no | — |
| `PaymentAddress.City` | body | `string` | no | — |
| `SortName` | body | `string` | no | — |
| `Name` | body | `string` | no | — |
| `PaymentAddress.State` | body | `string` | no | — |
| `PaymentAddress.Zip` | body | `string` | no | — |
| `Type` | body | `string` | no | — |
| `PaymentAddress` | body | `object` | no | — |
| `PaymentAddress.Country` | body | `string` | no | — |
| `PaymentAddress.AddnlInfo` | body | `string` | no | — |
| `PurchasingAddress` | body | `object` | no | — |
| `PayTerms` | body | `string` | no | — |
| `CompanyContact` | body | `object` | no | — |
| `PayTerms` | body | `string` | no | — |
| `__custom_fields` | body | `object` | no | "__custom_fields": {     "newKey": "New Value",     "newKey-1": "New Value"   } |
