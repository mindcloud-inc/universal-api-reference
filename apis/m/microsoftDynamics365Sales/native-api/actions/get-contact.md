# Get Contact with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts(:contactId)`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [Get Contact](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/reference/entities/contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | — |
| `$select` | query | `string` | no | Comma-separated column logical names to return. Send multiple values as a string separated by `,`. |
| `$expand` | query | `string` | no | OData relationship expression specifying related records to include. |
