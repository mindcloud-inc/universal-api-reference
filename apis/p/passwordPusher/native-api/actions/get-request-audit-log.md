# Get Request Audit Log with Password Pusher

Retrieves a request audit log from Password Pusher.

## Endpoint

- **Method:** `GET`
- **Path:** `/requests/{{urlToken}}/audit`
- **Base URL:** `https://eu.pwpush.com/api/v2`
- **Official documentation:** [Get Request Audit Log](https://eu.pwpush.com/help/api/requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlToken` | path | `string` | yes | The request URL token owned by the authenticated account. |
