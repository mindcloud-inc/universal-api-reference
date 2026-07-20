# Update Meeting Type with Avoma

Updates an existing meeting type in Avoma.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/meeting_type/:uuid/`
- **Base URL:** `https://api.avoma.com`
- **Official documentation:** [Update Meeting Type](https://dev.avoma.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Unique ID of the meeting type. |
| `label` | body | `string` | no | Updated label of the meeting type. |
| `description` | body | `string` | no | Updated description of the meeting type. |
