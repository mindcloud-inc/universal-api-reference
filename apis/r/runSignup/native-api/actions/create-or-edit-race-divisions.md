# Create or Edit Race Divisions with RunSignup

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/divisions/manage-divisions.json`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [Create or Edit Race Divisions](https://runsignup.com/API/v2/divisions/manage-divisions.json/POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | query | `number` | yes | Race ID. |
| `event_id` | query | `number` | yes | Event ID. |
| `result_set_id` | query | `number` | no | Result set ID to associate with all divisions in the request. |
| `request` | body | `string` | yes | — |
