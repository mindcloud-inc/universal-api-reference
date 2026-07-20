# Get Security Settings with NextDNS

Retrieves security settings for a NextDNS profile.

## Endpoint

- **Method:** `GET`
- **Path:** `/profiles/:profile/security`
- **Base URL:** `https://api.nextdns.io`
- **Official documentation:** [Get Security Settings](https://nextdns.io/api#nested-objects-and-arrays)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | path | `string` | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |
