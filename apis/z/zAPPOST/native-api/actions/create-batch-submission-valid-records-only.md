# Create Batch Submission Valid Records Only with ZAP POST

Creates a batch submission using only valid records.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/submissions`
- **Base URL:** `https://api.zappost.com`
- **Official documentation:** [Create Batch Submission Valid Records Only](https://apidocumentation.zappost.com/api-endpoints/submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | yes | The campaign UUID to submit the records against. |
| `submissions[]` | body | `array<object>` | yes | Provide one or more submission records in the array for the /submissions endpoint. |
