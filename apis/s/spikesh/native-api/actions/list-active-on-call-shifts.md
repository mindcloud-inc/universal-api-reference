# List Active On-Call Shifts with Spike.sh

Retrieves active on-call shifts from Spike.sh.

## Endpoint

- **Method:** `GET`
- **Path:** `/oncalls/all-active-on-call-shifts`
- **Base URL:** `https://api.spike.sh`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | Spike.sh team ID used to populate the x-team-id request header for team-scoped endpoints. |
