# Update Lead with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `PATCH`
- **Path:** `/leads(:leadId)`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [Update Lead](https://learn.microsoft.com/en-us/dynamics365/developer/reference/entities/lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadId` | path | `string` | yes | — |
| `fields` | body | `object` | no | Map an object containing only the columns to change, or fill the individual fields below. Use native column logical names for custom fields. |
| `fields.subject` | body | `string` | no | — |
| `fields.firstname` | body | `string` | no | — |
| `fields.lastname` | body | `string` | no | — |
| `fields.middlename` | body | `string` | no | — |
| `fields.jobtitle` | body | `string` | no | — |
| `fields.emailaddress1` | body | `string` | no | — |
| `fields.mobilephone` | body | `string` | no | — |
| `fields.telephone1` | body | `string` | no | — |
| `fields.description` | body | `string` | no | — |
| `fields.donotemail` | body | `boolean` | no | — |
| `fields.donotphone` | body | `boolean` | no | — |
| `fields.companyname` | body | `string` | no | — |
| `fields.websiteurl` | body | `string` | no | — |
| `fields.revenue` | body | `number` | no | — |
| `fields.numberofemployees` | body | `number` | no | — |
| `fields.address1_line1` | body | `string` | no | — |
| `fields.address1_line2` | body | `string` | no | — |
| `fields.address1_city` | body | `string` | no | — |
| `fields.address1_stateorprovince` | body | `string` | no | — |
| `fields.address1_postalcode` | body | `string` | no | — |
| `fields.address1_country` | body | `string` | no | — |
| `$select` | query | `string` | no | Comma-separated column logical names to return. Send multiple values as a string separated by `,`. |
