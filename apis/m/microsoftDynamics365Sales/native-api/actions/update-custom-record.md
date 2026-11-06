# Update Custom Record with Microsoft Dynamics 365 Sales

## Endpoint

- **Method:** `PATCH`
- **Path:** `/:entitySetName(:recordId)`
- **Base URL:** `{environmentUrl}/api/data/v9.2`
- **Official documentation:** [Update Custom Record](https://learn.microsoft.com/en-us/power-apps/developer/data-platform/webapi/update-delete-entities-using-web-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `entitySetName` | path | `string` | yes | EntitySetName returned by List Tables. Use this exact API collection name, not the display label or a guessed plural. |
| `recordId` | path | `string` | yes | — |
| `fields` | body | `object` | yes | An object mapping the custom table's column logical names to their new values. Use List Table Columns to find writable columns. This schema varies by your environment. |
| `$select` | query | `string` | no | Comma-separated column logical names to return. Send multiple values as a string separated by `,`. |
