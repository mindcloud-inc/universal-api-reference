# List Integrations with Spike.sh

Retrieves integrations for a team in Spike.sh.

## Endpoint

- **Method:** `GET`
- **Path:** `/integrations`
- **Base URL:** `https://api.spike.sh`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Spike.sh team ID used to populate the x-team-id request header for team-scoped endpoints. |
