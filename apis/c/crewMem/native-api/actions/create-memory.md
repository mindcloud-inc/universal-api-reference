# Create Memory with CrewMem

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/memory/create`
- **Base URL:** `https://crewmem.com`
- **Official documentation:** [Create Memory](https://crewmem.com/docs/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Member email |
| `external_id` | body | `string` | no | External member ID |
| `fullname` | body | `string` | yes | Member full name |
| `input_data` | body | `string` | yes | Memory content to add |
| `integration_source` | body | `string` | no | Integration source |
| `team_name` | body | `string` | yes | Target team name |
| `team_type` | body | `string` | no | Target team type |
| `title` | body | `string` | yes | Member title |
