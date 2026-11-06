# Get Lead with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `GET`
- **Path:** `/leads(:leadId)`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [Get Lead](https://learn.microsoft.com/en-us/dynamics365/developer/reference/entities/lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `leadId` | path | `string` | yes | — |
| `$select` | query | `string` | no | Comma-separated column logical names to return. Send multiple values as a string separated by `,`. |
| `$expand` | query | `string` | no | OData relationship expression specifying related records to include. |
