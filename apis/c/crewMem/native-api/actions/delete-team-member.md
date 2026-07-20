# Delete Team Member with CrewMem

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/team-member/delete`
- **Base URL:** `https://crewmem.com`
- **Official documentation:** [Delete Team Member](https://crewmem.com/docs/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Member email |
| `team_name` | body | `string` | yes | Target team name |
