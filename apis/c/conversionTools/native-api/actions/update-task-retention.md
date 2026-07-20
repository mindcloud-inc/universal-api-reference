# Update Task Retention with Conversion Tools

Updates an existing task retention mode in Conversion Tools.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/tasks/:taskId/retention`
- **Base URL:** `https://api.conversiontools.io/v1`
- **Official documentation:** [Update Task Retention](https://api.conversiontools.io/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskId` | path | `string` | yes | The task ID to update. |
| `retentionMode` | body | `list<string>` | yes | Retention mode to apply to the task files. `ttl_15m` is only available on paid Conversion Tools plans. Accepted values: `standard_24h`, `ttl_15m`. |
