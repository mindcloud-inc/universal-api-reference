# Create Batch Submission For Specific Scheduled Send with ZAP POST

Creates a batch submission for a specific scheduled send.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/submissions`
- **Base URL:** `https://api.zappost.com`
- **Official documentation:** [Create Batch Submission For Specific Scheduled Send](https://apidocumentation.zappost.com/api-endpoints/submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | yes | The campaign UUID to submit the records against. |
| `scheduledSendDateId` | body | `string` | yes | The specific scheduled send UUID to use. |
| `submissions[]` | body | `array<object>` | yes | Provide one or more submission records in the array for the /submissions endpoint. |
