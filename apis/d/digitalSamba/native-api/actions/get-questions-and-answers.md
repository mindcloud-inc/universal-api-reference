# Get questions and answers with Digital Samba

Retrieves room questions and answers from Digital Samba.

## Endpoint

- **Method:** `GET`
- **Path:** `/rooms/:room/questions`
- **Base URL:** `https://api.digitalsamba.com/api/v1`
- **Official documentation:** [Get questions and answers](https://developer.digitalsamba.com/rest-api/#rooms-GETapi-v1-rooms--room--questions)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `room` | path | `string` | yes | Room path parameter. |
| `session_id` | query | `string` | no | UUID of the session. |
| `after` | query | `string` | no | The UUID of the question after which records will be returned. |
