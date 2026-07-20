# Get Snapshot Build Logs URL with Daytona

Retrieves the snapshot build logs URL from Daytona.

## Endpoint

- **Method:** `GET`
- **Path:** `/snapshots/[:id]/build-logs-url`
- **Base URL:** `https://app.daytona.io/api`
- **Official documentation:** [Get Snapshot Build Logs URL](https://www.daytona.io/docs/tools/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Snapshot ID or name. |
