# List Alert Rules with Spike.sh

Retrieves alert rules for a team in Spike.sh.

## Endpoint

- **Method:** `GET`
- **Path:** `/automation/rules`
- **Base URL:** `https://api.spike.sh`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Spike.sh team ID used to populate the x-team-id request header for team-scoped endpoints. |
