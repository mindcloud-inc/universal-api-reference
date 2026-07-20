# Check Customer Key Exists with Walla Form

## Endpoint

- **Method:** `GET`
- **Path:** `/workspace/:workspaceKey/project/:projectKey/response/check/customerKey/:customerKey`
- **Base URL:** `https://walla-api.data-lab.workers.dev`
- **Official documentation:** [Check Customer Key Exists](https://walla-api.data-lab.workers.dev/ui)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceKey` | path | `string` | yes | The Walla workspace key. |
| `projectKey` | path | `string` | yes | The Walla project key. |
| `customerKey` | path | `string` | yes | The customer key recorded in the Walla response. |
