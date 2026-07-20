# Get Project Progress with Leantime

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `{workspaceUrl}/api/jsonrpc`
- **Official documentation:** [Get Project Progress](https://docs.leantime.io/api/classes/Leantime/Domain/Projects/Services/Projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `params.projectId` | body | `number` | yes | The project ID whose progress should be calculated. |
