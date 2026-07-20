# Get Response by Response Key with Walla Form

## Endpoint

- **Method:** `GET`
- **Path:** `/workspace/:workspaceKey/project/:projectKey/response/get/responseKey/:responseKey`
- **Base URL:** `https://walla-api.data-lab.workers.dev`
- **Official documentation:** [Get Response by Response Key](https://walla-api.data-lab.workers.dev/ui)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceKey` | path | `string` | yes | The Walla workspace key. |
| `projectKey` | path | `string` | yes | The Walla project key. |
| `responseKey` | path | `string` | yes | The response key returned by Walla. |
