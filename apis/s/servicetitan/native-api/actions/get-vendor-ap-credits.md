# Get Vendor AP Credits with ServiceTitan

Retrieves vendor bills from ServiceTitan.

## Endpoint

- **Method:** `GET`
- **Path:** `accounting/v2/tenant/{tenant}/ap-credits`
- **Base URL:** `https://{baseUrl}/`
- **Official documentation:** [Get Vendor AP Credits](https://developer.servicetitan.io/docs/apis/tenant-accounting-v2/endpoints/ApCredits_GetList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ids` | query | `string` | no | Comma-separated list of specific AP credit IDs to retrieve Send multiple values as a string separated by `,`. |
| `page` | query | `number` | no | The logical page number to return, starting from 1 |
| `pageSize` | query | `number` | no | How many records to return (50 by default) |
| `includeTotal` | query | `boolean` | no | Whether total count should be returned |
| `createdBefore` | query | `date` | no | Return items created before certain date/time (in UTC) |
| `createdOnOrAfter` | query | `date` | no | Return items created on or after certain date/time (in UTC) |
| `modifiedBefore` | query | `date` | no | Return items modified before certain date/time (in UTC) |
| `modifiedOnOrAfter` | query | `date` | no | Return items modified on or after certain date/time (in UTC) |
| `sort` | query | `string` | no | Applies sorting by specified fields |
| `customField.Fields` | query | `object` | no | Dictionary of custom-field name-value pairs |
| `customField.Operator` | query | `list<string>` | no | Operator between custom-field name-value pairs. Values: And, Or; default: And. Accepted values: `And`, `Or`. |
| `syncStatuses` | query | `list<string>` | no | Filter by sync status values Accepted values: `Exported`, `Pending`, `Posted`, `PostedAndExported`. Send multiple values as a array. |
