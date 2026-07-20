# Run Project with Hex

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:projectId/runs`
- **Base URL:** `https://app.hex.tech/api/v1`
- **Official documentation:** [Run Project](https://learn.hex.tech/docs/api-integrations/api/reference#operation/RunProject)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dryRun` | body | `boolean` | no | Whether to trigger the project run as a dry run. |
| `projectId` | path | `string` | yes | Unique ID for a Hex project. |
| `updateCache` | body | `boolean` | no | — |
| `updatePublishedResults` | body | `boolean` | no | — |
| `useCachedSqlResults` | body | `boolean` | no | — |
| `viewId` | body | `string` | no | — |
