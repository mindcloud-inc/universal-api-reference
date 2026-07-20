# Attach File with SmartSuite

Attaches a file to a SmartSuite record.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/applications/:tableId/records/:recordId/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Attach File](https://developers.smartsuite.com/docs/solution-data/records/attach-file)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tableId` | path | `string` | yes | The SmartSuite table ID containing the target record. |
| `recordId` | path | `string` | yes | The SmartSuite record ID to update with the file attachment. |
| `fileFieldSlug` | body | `string` | yes | The file field slug that should receive the attached file URL. |
| `fileUrl` | body | `string` | yes | A publicly reachable file URL for SmartSuite to fetch and attach. |
