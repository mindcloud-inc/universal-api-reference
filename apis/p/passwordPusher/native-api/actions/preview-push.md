# Preview Push with Password Pusher

Retrieves a push URL preview from Password Pusher.

## Endpoint

- **Method:** `GET`
- **Path:** `/pushes/{{urlToken}}/preview`
- **Base URL:** `https://eu.pwpush.com/api/v2`
- **Official documentation:** [Preview Push](https://eu.pwpush.com/help/api/pushes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlToken` | path | `string` | yes | The push URL token from the secret URL. |
