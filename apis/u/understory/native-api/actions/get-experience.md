# Get Experience with Understory

Retrieves an experience from Understory.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/experiences/{{experienceId}}`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [Get Experience](https://developer.understory.io/apis/experience/getexperiencebyid.md)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept-Language` | `en-GB` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experienceId` | path | `string` | yes | The unique identifier of the experience. |
