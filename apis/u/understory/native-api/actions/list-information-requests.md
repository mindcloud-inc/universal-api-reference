# List Information Requests with Understory

Retrieves information requests for an experience in Understory.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/experiences/{{experienceId}}/information-requests`
- **Base URL:** `https://api.understory.io`
- **Official documentation:** [List Information Requests](https://developer.understory.io/apis/experience/getinformationrequestsforexperience.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept-Language` | `en-GB` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `experienceId` | path | `string` | yes | The unique identifier of the experience. |
