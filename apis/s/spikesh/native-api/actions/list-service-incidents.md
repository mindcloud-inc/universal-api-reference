# List Service Incidents with Spike.sh

Retrieves incidents for a service in Spike.sh.

## Endpoint

- **Method:** `GET`
- **Path:** `/services/:counterId/incidents`
- **Base URL:** `https://api.spike.sh`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `counterId` | path | `string` | yes | Spike.sh service counterId. |
| `teamId` | path | `string` | yes | Spike.sh team ID used to populate the x-team-id request header for team-scoped endpoints. |
