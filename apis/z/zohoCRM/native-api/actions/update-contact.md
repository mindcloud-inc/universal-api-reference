# Update Contact with Zoho CRM

Updates an existing contact in Zoho CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Contacts`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Update Contact](https://www.zoho.com/crm/developer/docs/api/v8/update-records.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array<object>` | yes | Contact records to update. |
| `data[].id` | body | `string` | yes | — |
| `data[].Last_Name` | body | `string` | no | — |
| `data[].Email` | body | `string` | no | — |
| `data[].A2Z_Contact_ID` | body | `string` | no | — |
| `data[].Company` | body | `string` | no | — |
| `data[].First_Name` | body | `string` | no | — |
| `data[].Middle_Name` | body | `string` | no | — |
| `data[].Title` | body | `string` | no | — |
| `data[].Website` | body | `string` | no | — |
| `data[].Mailing_City` | body | `string` | no | — |
| `data[].Mailing_Country` | body | `string` | no | — |
| `data[].Mailing_Zip` | body | `string` | no | — |
| `data[].Mailing_State` | body | `string` | no | — |
| `data[].Mailing_Street` | body | `string` | no | — |
| `data[].Mailing_Street_2` | body | `string` | no | — |
| `data[].Account_Name` | body | `string` | no | — |
| `data[].Contact_Type` | body | `string` | no | — |
| `data[].TPE27_Confirmed_Exhibitor` | body | `boolean` | no | — |
| `data[].Confirmed_Exhibitor` | body | `boolean` | no | — |
