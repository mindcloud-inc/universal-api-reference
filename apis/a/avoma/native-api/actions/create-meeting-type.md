# Create Meeting Type with Avoma

Creates a new meeting type in Avoma.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/meeting_type/`
- **Base URL:** `https://api.avoma.com`
- **Official documentation:** [Create Meeting Type](https://dev.avoma.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `label` | body | `string` | yes | Label of the meeting type. |
| `description` | body | `string` | no | Description of the meeting type. |
