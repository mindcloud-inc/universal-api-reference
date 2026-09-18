# Update Account with Zoho CRM

Updates an existing account in Zoho CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Accounts`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Update Account](https://www.zoho.com/crm/developer/docs/api/v8/update-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Account records to update. |
| `data[].A2ZAccountID` | body | `string` | no | — |
| `data[].id` | body | `string` | yes | — |
| `data[].Shipping_Postcode` | body | `string` | no | — |
| `data[].Shipping_Street_2` | body | `string` | no | — |
| `data[].Account_Name` | body | `string` | no | — |
| `data[].Account_Name` | body | `string` | no | — |
| `data[].Website` | body | `string` | no | — |
| `data[].Shipping_Street` | body | `string` | no | — |
| `data[].Shipping_City` | body | `string` | no | — |
| `data[].Shipping_State` | body | `string` | no | — |
| `data[].Billing_Street` | body | `string` | no | — |
| `data[].Street_2` | body | `string` | no | — |
| `data[].Billing_City` | body | `string` | no | — |
| `data[].Billing_State` | body | `string` | no | — |
| `data[].Post_Code` | body | `string` | no | — |
| `data[].Billing_Country` | body | `string` | no | — |
| `data[].Acct_Typ` | body | `list` | no | Accepted values: `Advertisor`, `Association`, `Attendee`, `Confirmed Exhibitor`, `Exhibitor`, `Lead`, `Subscriber`. Send multiple values as a array. |
