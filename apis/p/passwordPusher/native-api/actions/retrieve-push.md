# Retrieve Push with Password Pusher

Retrieves a push payload from Password Pusher.

## Endpoint

- **Method:** `GET`
- **Path:** `/pushes/{{urlToken}}`
- **Base URL:** `https://eu.pwpush.com/api/v2`
- **Official documentation:** [Retrieve Push](https://eu.pwpush.com/help/api/pushes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlToken` | path | `string` | yes | The push URL token from the secret URL. |
| `passphrase` | query | `string` | no | Optional passphrase for passphrase-protected pushes. |
