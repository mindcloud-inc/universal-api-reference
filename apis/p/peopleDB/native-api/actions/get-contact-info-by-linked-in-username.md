# Get Contact Info by LinkedIn Username with PeopleDB

Retrieves contact info from PeopleDB by LinkedIn username.

## Endpoint

- **Method:** `GET`
- **Path:** `/people`
- **Base URL:** `https://peopledb.co/api/v1`
- **Official documentation:** [Get Contact Info by LinkedIn Username](https://docs.peopledb.co/openapi.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `linkedin_public_identifier` | query | `string` | yes | LinkedIn public identifier (username) to search by. |
