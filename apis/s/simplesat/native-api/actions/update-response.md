# Update Response with Simplesat

Updates an existing response in Simplesat.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/responses/:response_id/update`
- **Base URL:** `https://api.simplesat.io`
- **Official documentation:** [Update Response](https://developer.simplesat.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `response_id` | path | `string` | yes | The ID of the response to update |
| `survey_id` | body | `number` | yes | — |
| `tags[]` | body | `array<string>` | no | — |
| `answers[]` | body | `array<object>` | no | — |
| `team_members[]` | body | `array<object>` | no | — |
| `ticket` | body | `object` | no | — |
| `customer` | body | `object` | no | — |
