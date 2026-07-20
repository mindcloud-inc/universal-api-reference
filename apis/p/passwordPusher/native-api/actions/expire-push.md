# Expire Push with Password Pusher

Expires an existing push in Password Pusher.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/pushes/{{urlToken}}`
- **Base URL:** `https://eu.pwpush.com/api/v2`
- **Official documentation:** [Expire Push](https://eu.pwpush.com/help/api/pushes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlToken` | path | `string` | yes | The push URL token to expire. |
