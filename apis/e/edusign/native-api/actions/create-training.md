# Create Training with Edusign

Creates a new training in Edusign.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/trainings/`
- **Base URL:** `https://ext.edusign.fr`
- **Official documentation:** [Create Training](https://developers.edusign.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `NAME` | body | `string` | yes | Training name |
| `START` | body | `string` | yes | Start date of the training |
| `END` | body | `string` | yes | End date of the training (format YYYY-MM-DD HH:mm:ss, ISO 8601) |
| `GOALS` | body | `string` | no | Training goals |
| `TAGS[]` | body | `array<string>` | no | — |
| `STUDENTS[]` | body | `array<string>` | no | — |
| `API_ID` | body | `string` | no | The ID of your API resource representing the training |
| `API_TYPE` | body | `string` | no | The name of your API from where you created the training |
