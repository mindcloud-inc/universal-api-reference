# Retrieve Request with Password Pusher

Retrieves a request response from Password Pusher.

## Endpoint

- **Method:** `GET`
- **Path:** `/requests/{{urlToken}}`
- **Base URL:** `https://eu.pwpush.com/api/v2`
- **Official documentation:** [Retrieve Request](https://eu.pwpush.com/help/api/requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlToken` | path | `string` | yes | The request URL token from the secret URL. |
| `passphrase` | query | `string` | no | Optional passphrase for passphrase-protected requests. |
