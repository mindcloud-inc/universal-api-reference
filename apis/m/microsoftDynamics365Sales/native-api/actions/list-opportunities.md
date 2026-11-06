# List Opportunities with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `GET`
- **Path:** `/opportunities`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [List Opportunities](https://learn.microsoft.com/en-us/dynamics365/developer/reference/entities/opportunity)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | OData expression selecting matching records. |
| `$select` | query | `string` | no | Comma-separated column logical names to return. Send multiple values as a string separated by `,`. |
| `$expand` | query | `string` | no | OData relationship expression specifying related records to include. |
| `$count` | query | `boolean` | no | — |
