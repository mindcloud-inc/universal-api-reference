# Delete Race Divisions with RunSignup

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/divisions/delete-divisions.json`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [Delete Race Divisions](https://runsignup.com/API/v2/divisions/delete-divisions.json/POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | query | `number` | yes | Race ID. |
| `event_id` | query | `number` | yes | Event ID. |
| `request` | body | `string` | yes | — |
