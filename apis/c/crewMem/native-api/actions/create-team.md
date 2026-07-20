# Create Team with CrewMem

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/team/create`
- **Base URL:** `https://crewmem.com`
- **Official documentation:** [Create Team](https://crewmem.com/docs/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Team description |
| `external_id` | body | `string` | no | External team ID |
| `integration_source` | body | `string` | no | Integration source |
| `name` | body | `string` | yes | Team name |
| `type` | body | `string` | yes | Team type |
