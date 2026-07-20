# List Lookup Values with Supabugs

Retrieves issue lookup values from Supabugs.

## Endpoint

- **Method:** `GET`
- **Path:** `/lov`
- **Base URL:** `https://api.supabugs.io/api/public/v1`
- **Official documentation:** [List Lookup Values](https://api.supabugs.io/api/public/v1/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Lookup type: bug_type, bug_severity, bug_priority, or bug_status. |
