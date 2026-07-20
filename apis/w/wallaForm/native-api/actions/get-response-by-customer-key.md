# Get Response by Customer Key with Walla Form

## Endpoint

- **Method:** `GET`
- **Path:** `/workspace/:workspaceKey/project/:projectKey/response/get/customerKey/:customerKey`
- **Base URL:** `https://walla-api.data-lab.workers.dev`
- **Official documentation:** [Get Response by Customer Key](https://walla-api.data-lab.workers.dev/ui)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceKey` | path | `string` | yes | The Walla workspace key. |
| `projectKey` | path | `string` | yes | The Walla project key. |
| `customerKey` | path | `string` | yes | The customer key recorded in the Walla response. |
