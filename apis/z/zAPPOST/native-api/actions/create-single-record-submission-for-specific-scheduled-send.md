# Create Single Record Submission For Specific Scheduled Send with ZAP POST

Creates a single-record submission for a specific scheduled send.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/records`
- **Base URL:** `https://api.zappost.com`
- **Official documentation:** [Create Single Record Submission For Specific Scheduled Send](https://apidocumentation.zappost.com/api-endpoints/submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | yes | The campaign UUID to submit the record against. |
| `scheduledSendDateId` | body | `string` | yes | The specific scheduled send UUID to use. |
| `submissions[]` | body | `array<object>` | yes | Provide a single submission record in the array for the /records endpoint. |
