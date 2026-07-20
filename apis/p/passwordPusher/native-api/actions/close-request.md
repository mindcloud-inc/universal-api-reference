# Close Request with Password Pusher

Closes an existing request in Password Pusher.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/requests/{{urlToken}}`
- **Base URL:** `https://eu.pwpush.com/api/v2`
- **Official documentation:** [Close Request](https://eu.pwpush.com/help/api/requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urlToken` | path | `string` | yes | The request URL token to close. |
