# Get Opportunity with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `GET`
- **Path:** `/opportunities(:opportunityId)`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [Get Opportunity](https://learn.microsoft.com/en-us/dynamics365/developer/reference/entities/opportunity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `opportunityId` | path | `string` | yes | — |
| `$select` | query | `string` | no | Comma-separated column logical names to return. Send multiple values as a string separated by `,`. |
| `$expand` | query | `string` | no | OData relationship expression specifying related records to include. |
