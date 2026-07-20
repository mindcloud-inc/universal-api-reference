# List Acknowledged Incidents with Spike.sh

Retrieves acknowledged incidents for a team in Spike.sh.

## Endpoint

- **Method:** `GET`
- **Path:** `/incidents/acknowledged`
- **Base URL:** `https://api.spike.sh`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Spike.sh team ID used to populate the x-team-id request header for team-scoped endpoints. |
