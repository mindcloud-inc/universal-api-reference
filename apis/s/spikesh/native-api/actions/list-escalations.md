# List Escalations with Spike.sh

Retrieves all escalation policies from Spike.sh.

## Endpoint

- **Method:** `GET`
- **Path:** `/escalations`
- **Base URL:** `https://api.spike.sh`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Spike.sh team ID used to populate the x-team-id request header for team-scoped endpoints. |
