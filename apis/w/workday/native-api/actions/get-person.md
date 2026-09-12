# Get Person with Workday

Get a single person from the Workday Person API by Workday person ID.

## Endpoint

- **Method:** `GET`
- **Path:** `people/:ID`
- **Base URL:** `{restAPIBaseURL}/`
- **Official documentation:** [Get Person](https://community.workday.com/sites/default/files/file-hosting/restapi/index.html#person/v4/get-/people/-ID-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ID` | path | `string` | yes | The Workday person ID. You can use a returned person id from Get Workers or Get People. |
