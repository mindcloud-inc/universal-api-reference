# List On-Calls with Spike.sh

Retrieves on-call schedules for a team in Spike.sh.

## Endpoint

- **Method:** `GET`
- **Path:** `/on-calls`
- **Base URL:** `https://api.spike.sh`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Spike.sh team ID used to populate the x-team-id request header for team-scoped endpoints. |
