# Create Single Record Submission Valid Records Only with ZAP POST

Creates a single-record submission using only valid records.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/records`
- **Base URL:** `https://api.zappost.com`
- **Official documentation:** [Create Single Record Submission Valid Records Only](https://apidocumentation.zappost.com/api-endpoints/submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | yes | The campaign UUID to submit the record against. |
| `submissions[]` | body | `array<object>` | yes | Provide a single submission record in the array for the /records endpoint. |
