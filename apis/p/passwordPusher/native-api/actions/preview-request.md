# Preview Request with Password Pusher

Retrieves a request URL preview from Password Pusher.

## Endpoint

- **Method:** `GET`
- **Path:** `/requests/{{urlToken}}/preview`
- **Base URL:** `https://eu.pwpush.com/api/v2`
- **Official documentation:** [Preview Request](https://eu.pwpush.com/help/api/requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlToken` | path | `string` | yes | The request URL token from the secret URL. |
