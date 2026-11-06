# List Contacts with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [List Contacts](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/reference/entities/contact)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | OData expression selecting matching records. |
| `$select` | query | `string` | no | Comma-separated column logical names to return. Send multiple values as a string separated by `,`. |
| `$expand` | query | `string` | no | OData relationship expression specifying related records to include. |
| `$count` | query | `boolean` | no | — |
