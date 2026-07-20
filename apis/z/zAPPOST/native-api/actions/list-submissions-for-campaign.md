# List Submissions For Campaign with ZAP POST

Retrieves submissions for a specific campaign from ZAP POST.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/submissions/:campaignId`
- **Base URL:** `https://api.zappost.com`
- **Official documentation:** [List Submissions For Campaign](https://apidocumentation.zappost.com/api-endpoints/submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `string` | yes | The campaign UUID to list submissions for. |
