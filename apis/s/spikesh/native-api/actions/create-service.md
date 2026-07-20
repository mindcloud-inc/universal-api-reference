# Create Service with Spike.sh

Creates a new service in Spike.sh.

## Endpoint

- **Method:** `POST`
- **Path:** `/services/create`
- **Base URL:** `https://api.spike.sh`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `desc` | body | `string` | no | Service description. |
| `name` | body | `string` | yes | Service name. |
| `teamId` | path | `string` | yes | Spike.sh team ID used to populate the x-team-id request header for team-scoped endpoints. |
