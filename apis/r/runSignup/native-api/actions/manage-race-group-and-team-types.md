# Manage Race Group and Team Types with RunSignup

## Endpoint

- **Method:** `POST`
- **Path:** `/race/:race_id/teams/team-types`
- **Base URL:** `https://api.runsignup.com/rest`
- **Official documentation:** [Manage Race Group and Team Types](https://runsignup.com/API/race/:race_id/teams/team-types/POST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `race_id` | path | `string` | yes | Path parameter: race_id |
| `race_event_days_id` | query | `number` | yes | Race event days ID.  This ID groups together events, typically by year.  This ID is returned with the event information in the APIs to get races or a single race. |
| `request` | body | `string` | yes | — |
