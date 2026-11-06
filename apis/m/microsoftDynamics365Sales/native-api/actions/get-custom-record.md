# Get Custom Record with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `GET`
- **Path:** `/:entitySetName(:recordId)`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [Get Custom Record](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/webapi/retrieve-entity-using-web-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entitySetName` | path | `string` | yes | EntitySetName returned by List Tables. Use this exact API collection name, not the display label or a guessed plural. |
| `recordId` | path | `string` | yes | — |
| `$select` | query | `string` | no | Comma-separated column logical names to return. Send multiple values as a string separated by `,`. |
| `$expand` | query | `string` | no | OData relationship expression specifying related records to include. |
