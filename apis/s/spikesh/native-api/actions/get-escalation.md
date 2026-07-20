# Get Escalation with Spike.sh

Retrieves escalation policy details from Spike.sh.

## Endpoint

- **Method:** `GET`
- **Path:** `/escalations/:escalationId`
- **Base URL:** `https://api.spike.sh`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `escalationId` | path | `string` | yes | Spike.sh escalation ID. |
| `teamId` | path | `string` | yes | Spike.sh team ID used to populate the x-team-id request header for team-scoped endpoints. |
