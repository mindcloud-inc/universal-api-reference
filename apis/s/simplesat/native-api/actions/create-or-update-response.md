# Create or Update Response with Simplesat

Creates or updates a response in Simplesat.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/responses/create-or-update`
- **Base URL:** `https://api.simplesat.io`
- **Official documentation:** [Create or Update Response](https://developer.simplesat.io/api)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `survey_id` | body | `number` | yes |
| `tags[]` | body | `array<string>` | no |
| `answers[]` | body | `array<object>` | no |
| `team_members[]` | body | `array<object>` | no |
| `ticket` | body | `object` | no |
| `customer` | body | `object` | no |
