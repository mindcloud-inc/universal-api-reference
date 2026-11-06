# Update Account with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `PATCH`
- **Path:** `/accounts(:accountId)`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [Update Account](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/reference/entities/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | — |
| `fields` | body | `object` | no | Map an object containing only the columns to change, or fill the individual fields below. Use native column logical names for custom fields. |
| `fields.name` | body | `string` | no | — |
| `fields.accountnumber` | body | `string` | no | — |
| `fields.description` | body | `string` | no | — |
| `fields.emailaddress1` | body | `string` | no | — |
| `fields.telephone1` | body | `string` | no | — |
| `fields.telephone2` | body | `string` | no | — |
| `fields.websiteurl` | body | `string` | no | — |
| `fields.revenue` | body | `number` | no | — |
| `fields.numberofemployees` | body | `number` | no | — |
| `fields.creditlimit` | body | `number` | no | — |
| `fields.creditonhold` | body | `boolean` | no | — |
| `fields.donotemail` | body | `boolean` | no | — |
| `fields.donotphone` | body | `boolean` | no | — |
| `fields.address1_line1` | body | `string` | no | — |
| `fields.address1_line2` | body | `string` | no | — |
| `fields.address1_city` | body | `string` | no | — |
| `fields.address1_stateorprovince` | body | `string` | no | — |
| `fields.address1_postalcode` | body | `string` | no | — |
| `fields.address1_country` | body | `string` | no | — |
| `$select` | query | `string` | no | Comma-separated column logical names to return. Send multiple values as a string separated by `,`. |
