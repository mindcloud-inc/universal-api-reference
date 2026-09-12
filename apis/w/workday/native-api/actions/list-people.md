# List People with Workday

List people from the Workday Person API, optionally filtering by universal ID.

## Endpoint

- **Method:** `GET`
- **Path:** `people`
- **Base URL:** `{restAPIBaseURL}/`
- **Official documentation:** [List People](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#person/v4/get-/people)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `universal_ID` | query | `string` | no | Optional universal ID filter for the person you want to retrieve. |
