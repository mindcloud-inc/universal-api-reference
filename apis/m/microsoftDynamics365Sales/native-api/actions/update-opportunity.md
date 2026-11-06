# Update Opportunity with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `PATCH`
- **Path:** `/opportunities(:opportunityId)`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [Update Opportunity](https://learn.microsoft.com/en-us/dynamics365/developer/reference/entities/opportunity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opportunityId` | path | `string` | yes | — |
| `fields` | body | `object` | no | Map an object containing only the columns to change, or fill the individual fields below. Use native column logical names for custom fields. |
| `fields.name` | body | `string` | no | — |
| `fields.description` | body | `string` | no | — |
| `fields.estimatedvalue` | body | `number` | no | — |
| `fields.estimatedclosedate` | body | `date` | no | — |
| `fields.closeprobability` | body | `number` | no | — |
| `fields.budgetamount` | body | `number` | no | — |
| `fields.stepname` | body | `string` | no | — |
| `fields.isrevenuesystemcalculated` | body | `boolean` | no | — |
| `fields.currentsituation` | body | `string` | no | — |
| `fields.customerneed` | body | `string` | no | — |
| `fields.customerpainpoints` | body | `string` | no | — |
| `fields.proposedsolution` | body | `string` | no | — |
| `$select` | query | `string` | no | Comma-separated column logical names to return. Send multiple values as a string separated by `,`. |
