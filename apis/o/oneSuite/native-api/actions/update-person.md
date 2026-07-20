# Update Person with OneSuite

Updates a person in OneSuite.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/people/:people_id`
- **Base URL:** `https://api.onesuite.io`
- **Official documentation:** [Update Person](https://rest-api.onesuite.io/#update-people)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `people_id` | path | `string` | yes | People ID from the OneSuite update-people docs. |
| `name` | body | `string` | no | Updated full name for the person. |
