# Create or Edit Race Corrals with RunSignup

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/corrals/manage-corrals.json`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [Create or Edit Race Corrals](https://runsignup.com/API/v2/corrals/manage-corrals.json/POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | query | `number` | yes | Race ID. |
| `race_event_days_id` | query | `number` | yes | Race event days ID. |
| `request` | body | `string` | yes | — |
