# Create Meeting Outcome with Avoma

Creates a new meeting outcome in Avoma.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/meeting_outcome/`
- **Base URL:** `https://api.avoma.com`
- **Official documentation:** [Create Meeting Outcome](https://dev.avoma.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | body | `string` | yes | Label of the meeting outcome. |
| `description` | body | `string` | no | Description of the meeting outcome. |
