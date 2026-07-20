# List Session Recordings with Livestorm

Retrieves recordings for a session from Livestorm.

## Endpoint

- **Method:** `GET`
- **Path:** `sessions/:id/recordings`
- **Base URL:** `https://api.livestorm.co/v1`
- **Official documentation:** [List Session Recordings](https://developers.livestorm.co/reference/get_sessions-id-recordings)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Session ID |
| `url_expires_in` | query | `number` | no | Custom expiry time for signed URLs in seconds (1 hour to 7 days). Defaults to 12 hours (43200 seconds) if not provided. Must be a single integer value (e.g., `?url_expires_in=604800`), not a nested parameter. |
