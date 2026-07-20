# Create Batch Submission with ZAP POST

Creates a batch submission in a ZAP POST campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/submissions`
- **Base URL:** `https://api.zappost.com`
- **Official documentation:** [Create Batch Submission](https://apidocumentation.zappost.com/api-endpoints/submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | yes | The campaign UUID to submit the records against. |
| `onlyValidRecords` | body | `boolean` | no | When true, the request only succeeds if every record is valid. |
| `submissions[]` | body | `array<object>` | yes | Provide one or more submission records in the array for the /submissions endpoint. |
