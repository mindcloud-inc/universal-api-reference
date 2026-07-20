# Create Single Record Submission with ZAP POST

Creates a single-record submission in a ZAP POST campaign.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/records`
- **Base URL:** `https://api.zappost.com`
- **Official documentation:** [Create Single Record Submission](https://apidocumentation.zappost.com/api-endpoints/submissions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | body | `string` | yes | The campaign UUID to submit the record against. |
| `onlyValidRecords` | body | `boolean` | no | When true, the request only succeeds if every record is valid. |
| `submissions[]` | body | `array<object>` | yes | Provide a single submission record in the array for the /records endpoint. |
