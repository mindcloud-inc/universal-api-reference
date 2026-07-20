# Create Member with CrewMem

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/member/create`
- **Base URL:** `https://crewmem.com`
- **Official documentation:** [Create Member](https://crewmem.com/docs/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Member email |
| `external_id` | body | `string` | no | External member ID |
| `fullname` | body | `string` | yes | Member full name |
| `integration_source` | body | `string` | no | Integration source |
| `title` | body | `string` | yes | Member title |
