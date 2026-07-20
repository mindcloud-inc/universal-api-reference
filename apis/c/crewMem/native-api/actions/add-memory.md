# Add Memory with CrewMem

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/memory/add`
- **Base URL:** `https://crewmem.com`
- **Official documentation:** [Add Memory](https://crewmem.com/docs/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Member email |
| `input_data` | body | `string` | yes | Memory content to add |
| `team_name` | body | `string` | yes | Target team name |
