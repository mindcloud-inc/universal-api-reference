# Create or Edit Race Teams with RunSignup

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/teams/manage-teams.json`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [Create or Edit Race Teams](https://runsignup.com/API/v2/teams/manage-teams.json/POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | query | `number` | yes | Race ID. |
| `event_ids` | query | `string` | yes | ID of event or list of event IDs separated by commas. |
| `request` | body | `string` | yes | — |
