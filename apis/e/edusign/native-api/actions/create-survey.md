# Create Survey with Edusign

Creates a new survey in Edusign.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/surveys`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [Create Survey](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `survey` | body | `string` | yes | Template ID of the survey |
| `students[]` | body | `array<string>` | yes | — |
| `professors[]` | body | `array<string>` | yes | — |
| `externals[]` | body | `array<string>` | yes | — |
| `sending_date` | body | `string` | yes | Sending date |
| `trainingId` | body | `string` | no | Training ID |
