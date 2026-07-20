# Update Service with Spike.sh

Updates an existing service in Spike.sh.

## Endpoint

- **Method:** `PUT`
- **Path:** `/services/:counterId/update`
- **Base URL:** `https://api.spike.sh`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `counterId` | path | `string` | yes | Spike.sh service counterId. |
| `desc` | body | `string` | no | Updated service description. |
| `name` | body | `string` | yes | Updated service name. |
| `teamId` | path | `string` | yes | Spike.sh team ID used to populate the x-team-id request header for team-scoped endpoints. |
