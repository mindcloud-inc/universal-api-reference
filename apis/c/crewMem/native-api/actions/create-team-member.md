# Create Team Member with CrewMem

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/team-member/create`
- **Base URL:** `https://crewmem.com`
- **Official documentation:** [Create Team Member](https://crewmem.com/docs/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Member email |
| `external_id` | body | `string` | no | External member ID |
| `fullname` | body | `string` | yes | Member full name |
| `integration_source` | body | `string` | no | Integration source |
| `team_name` | body | `string` | yes | Target team name |
| `title` | body | `string` | yes | Member title |
