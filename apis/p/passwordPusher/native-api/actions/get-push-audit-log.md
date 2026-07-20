# Get Push Audit Log with Password Pusher

Retrieves a push audit log from Password Pusher.

## Endpoint

- **Method:** `GET`
- **Path:** `/pushes/{{urlToken}}/audit`
- **Base URL:** `https://eu.pwpush.com/api/v2`
- **Official documentation:** [Get Push Audit Log](https://eu.pwpush.com/help/api/pushes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlToken` | path | `string` | yes | The push URL token owned by the authenticated account. |
