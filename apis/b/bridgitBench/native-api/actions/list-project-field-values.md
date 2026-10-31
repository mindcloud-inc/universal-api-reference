# List Project Field Values with Bridgit Bench

## Endpoint

- **Method:** `GET`
- **Path:** `/rp/api/v1/accounts/:accountId/projects/:projectId/project-field-values`
- **Base URL:** `https://bench.gobridgit.com`
- **Official documentation:** [List Project Field Values](https://developers.gobridgit.com/reference/projectfieldvalue_queryfieldvalues)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | path | `number` | yes | The Account ID |
| `projectId` | path | `number` | yes | The project ID the role belongs to |
| `includeEmpty` | query | `boolean` | no | Returns fields with empty/unset value as well |
| `classification` | query | `list<string>` | no | Optional - for filtering result by classification: All or Experience" Accepted values: `All`, `Experience`. |
