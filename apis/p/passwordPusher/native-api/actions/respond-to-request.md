# Respond To Request with Password Pusher

Responds to an open request in Password Pusher.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/requests/{{urlToken}}/respond`
- **Base URL:** `https://eu.pwpush.com/api/v2`
- **Official documentation:** [Respond To Request](https://eu.pwpush.com/help/api/requests)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlToken` | path | `string` | yes | The request URL token to respond to. |
| `request.response` | body | `string` | yes | The response text to submit to the request. |
