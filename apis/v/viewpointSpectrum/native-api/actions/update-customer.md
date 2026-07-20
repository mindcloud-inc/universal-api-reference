# Update Customer with Viewpoint Spectrum

## Endpoint

- **Method:** `POST`
- **Path:** `ws/AddCustomer`
- **Base URL:** `{url}:8482/`
- **Official documentation:** [Update Customer](https://help.trimble.com/en/spectrum/spectrum/api-web-services/list-of-web-services/accounts-receivable-services/update-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `Customer_Code` | body | `string` | yes | Customer Code. |
| `Name` | body | `string` | no | Customer Name. |
| `Alpha_Sort` | body | `string` | no | Customer Alpha Ref. |
| `Type` | body | `string` | no | Customer Type. |
| `Address_1` | body | `string` | no | Address 1. |
| `Address_2` | body | `string` | no | Address 2. |
| `City` | body | `string` | no | City. |
| `State` | body | `string` | no | State. |
| `Zip_Code` | body | `string` | no | Zip Code. |
| `Phone` | body | `string` | no | Phone Number. |
| `Fax_Phone` | body | `string` | no | Fax number. |
| `Contact_1` | body | `string` | no | Contact 1. |
| `Contact_2` | body | `string` | no | Contact 2. |
| `Contact_3` | body | `string` | no | Contact 3. |
| `Salesperson` | body | `string` | no | Salesman Code. |
| `Terms_Code` | body | `string` | no | Terms Code. |
| `Standard_Retention_Percent` | body | `number` | no | Default Retention (Holdback) percent. |
| `Taxable_Flag` | body | `string` | no | Taxable flag (Y/N). |
| `Sales_Tax_Code` | body | `string` | no | Sales tax code. |
| `Resale_Number` | body | `string` | no | Resale certificate number. |
| `Resale_Exp_Date` | body | `date` | no | Resale expiration date. |
| `Statement_Flag` | body | `string` | no | Send statement flag (Y/N). |
| `Finance_Charge_Tran_Code` | body | `string` | no | Finance Charge Code. |
| `Finance_Charge` | body | `number` | no | Finance Charge percent. |
| `Price_Level_Material` | body | `number` | no | Work Order Material Level. |
| `Price_Level_Labor` | body | `number` | no | Work Order Labor Level. |
| `Credit_Limit` | body | `number` | no | Credit Limit. |
| `Date_Created` | body | `date` | no | Date Established. |
| `Customer_Email` | body | `string` | no | Customer Email. |
| `Markup_Code` | body | `string` | no | Non-stock Markup Code. |
| `userDefinedFields` | body | `object` | no | User-defined fields object for UDF1 through UDF20. |
