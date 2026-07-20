# Clear Logs with NextDNS

Deletes DNS logs from a NextDNS profile.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/profiles/:profile/logs`
- **Base URL:** `https://api.nextdns.io`
- **Official documentation:** [Clear Logs](https://nextdns.io/api#clear)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | path | `string` | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |
