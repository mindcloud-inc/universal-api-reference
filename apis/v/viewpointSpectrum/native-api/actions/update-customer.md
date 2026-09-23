# Update Customer with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `customer/updatecustomer`
- **Base URL:** `{url}:8482/`
- **Official documentation:** [Update Customer](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/add-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Address_1` | body | `string` | no | Maximum length: 30. |
| `Address_2` | body | `string` | no | Maximum length: 30. |
| `alphaSort` | body | `string` | no | — |
| `City` | body | `string` | no | Maximum length: 25. |
| `Customer_Code` | body | `string` | yes | Maximum length: 10. |
| `Name` | body | `string` | yes | Maximum length: 30. |
| `type` | body | `string` | no | Maximum length: 10. |
| `State` | body | `string` | no | Maximum length: 2. |
| `Zip_Code` | body | `string` | no | Maximum length: 10. |
| `Phone_Number` | body | `string` | no | Maximum length: 14. |
| `faxPhone` | body | `string` | no | Maximum length: 14. |
| `contact1` | body | `string` | no | Maximum length: 20. |
| `Contact_2` | body | `string` | no | Maximum length: 20. |
| `Contact_3` | body | `string` | no | Maximum length: 20. |
| `Salesperson` | body | `string` | no | Maximum length: 3. |
| `standardRetentionPercent` | body | `number` | no | — |
| `Taxable_Flag` | body | `list` | no | — |
| `resaleNumber` | body | `string` | no | Maximum length: 15. |
| `resaleExpDate` | body | `date` | no | — |
| `Statement_Flag` | body | `list` | no | — |
| `financeChargeTranCode` | body | `string` | no | — |
| `financeCharge` | body | `number` | no | — |
| `priceLevelMaterial` | body | `list<number>` | no | — |
| `priceLevelLabor` | body | `list<number>` | no | — |
| `creditLimit` | body | `number` | no | — |
| `dateCreated` | body | `date` | no | — |
| `Email1` | body | `string` | no | — |
| `markupCode` | body | `string` | no | — |
| `userDefinedFields` | body | `object` | no | UDF1 — UDF20 |
| `Terms_Code` | body | `string` | no | — |
| `Sales_Tax_Code` | body | `string` | no | — |
