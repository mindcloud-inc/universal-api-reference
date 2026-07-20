# Get Duty Summary with SIGNL4

Retrieves duty summaries from SIGNL4.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/duties/summary`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Get Duty Summary](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId[]` | query | `array<string>` | no | IDs of the teams to get the summaries for. |
| `lastTwoDuties` | query | `boolean` | no | Decide if you want all duties or only the last two. |
