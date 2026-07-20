# Get Contact Info by GitHub ID with PeopleDB

Retrieves contact info from PeopleDB by GitHub ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/people`
- **Base URL:** `https://peopledb.co/api/v1`
- **Official documentation:** [Get Contact Info by GitHub ID](https://docs.peopledb.co/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `github_id` | query | `number` | yes | GitHub numeric ID to search by. |
