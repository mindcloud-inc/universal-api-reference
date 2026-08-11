# Create Customer with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `ws/AddCustomer`
- **Base URL:** `{url}:8482/`
- **Official documentation:** [Create Customer](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/add-customer)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `text/xml; charset=utf-8` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address1` | body | `string` | no | Maximum length: 30. |
| `address2` | body | `string` | no | Maximum length: 30. |
| `alphaSort` | body | `string` | no | — |
| `city` | body | `string` | no | Maximum length: 25. |
| `customerCode` | body | `string` | yes | Maximum length: 10. |
| `name` | body | `string` | yes | Maximum length: 30. |
| `type` | body | `string` | no | Maximum length: 10. |
| `state` | body | `string` | no | Maximum length: 2. |
| `zipCode` | body | `string` | no | Maximum length: 10. |
| `phone` | body | `string` | no | Maximum length: 14. |
| `faxPhone` | body | `string` | no | Maximum length: 14. |
| `contact1` | body | `string` | no | Maximum length: 20. |
| `Contact_2` | body | `string` | no | Maximum length: 20. |
| `Contact_3` | body | `string` | no | Maximum length: 20. |
| `Salesperson` | body | `string` | no | Maximum length: 3. |
| `termsCode` | body | `string` | no | Maximum length: 1. |
| `standardRetentionPercent` | body | `number` | no | — |
| `taxableFlag` | body | `list` | no | — |
| `salesTaxCode` | body | `string` | no | Maximum length: 15. |
| `resaleNumber` | body | `string` | no | Maximum length: 15. |
| `resaleExpDate` | body | `date` | no | — |
| `statementFlag` | body | `list` | no | — |
| `financeChargeTranCode` | body | `string` | no | — |
| `financeCharge` | body | `number` | no | — |
| `priceLevelMaterial` | body | `list<number>` | no | — |
| `priceLevelLabor` | body | `list<number>` | no | — |
| `creditLimit` | body | `number` | no | — |
| `dateCreated` | body | `date` | no | — |
| `Email1` | body | `string` | no | — |
| `markupCode` | body | `string` | no | — |
| `userDefinedFields` | body | `object` | no | UDF1 — UDF20 |
