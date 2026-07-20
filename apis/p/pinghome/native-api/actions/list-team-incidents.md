# List Team Incidents with Pinghome

Retrieves team incidents from Pinghome.

## Endpoint

- **Method:** `GET`
- **Path:** `/incident-query/v1/team/:id/incidents`
- **Base URL:** `https://api.pinghome.io`
- **Official documentation:** [List Team Incidents](https://docs.pinghome.io/incident-management/incident-tracking/get-team-incidents/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Team ID for incident retrieval. |
