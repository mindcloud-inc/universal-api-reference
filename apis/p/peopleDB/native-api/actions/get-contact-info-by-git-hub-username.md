# Get Contact Info by GitHub Username with PeopleDB

Retrieves contact info from PeopleDB by GitHub username.

## Endpoint

- **Method:** `GET`
- **Path:** `/people`
- **Base URL:** `https://peopledb.co/api/v1`
- **Official documentation:** [Get Contact Info by GitHub Username](https://docs.peopledb.co/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `github_login` | query | `string` | yes | GitHub login (username) to search by. |
