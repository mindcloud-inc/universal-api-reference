# Check Bulk Lookup Progress with Enrich.so

Retrieves bulk profile lookup progress from Enrich.so.

## Endpoint

- **Method:** `GET`
- **Path:** `/reverse-lookup/bulk-lookup/{batchId}`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Check Bulk Lookup Progress](https://doc.enrich.so/check-bulk-lookup-progress-27483205e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `batchId` | path | `string` | yes | Bulk reverse lookup batch ID. |
