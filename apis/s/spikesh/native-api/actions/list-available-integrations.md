# List Available Integrations with Spike.sh

Retrieves all integrations available in Spike.sh.

## Endpoint

- **Method:** `GET`
- **Path:** `/integrations/available`
- **Base URL:** `https://api.spike.sh`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Spike.sh team ID used to populate the x-team-id request header for team-scoped endpoints. |
