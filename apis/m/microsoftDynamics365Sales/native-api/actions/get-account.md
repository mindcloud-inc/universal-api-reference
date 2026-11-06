# Get Account with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `GET`
- **Path:** `/accounts(:accountId)`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [Get Account](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/reference/entities/account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `string` | yes | — |
| `$select` | query | `string` | no | Comma-separated column logical names to return. Send multiple values as a string separated by `,`. |
| `$expand` | query | `string` | no | OData relationship expression specifying related records to include. |
