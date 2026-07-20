# Update Meeting Outcome with Avoma

Updates an existing meeting outcome in Avoma.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/meeting_outcome/:uuid/`
- **Base URL:** `https://api.avoma.com`
- **Official documentation:** [Update Meeting Outcome](https://dev.avoma.com)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | path | `string` | yes | Unique ID of the meeting outcome. |
| `label` | body | `string` | no | Updated label of the meeting outcome. |
| `description` | body | `string` | no | Updated description of the meeting outcome. |
