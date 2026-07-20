# List Allowlist with NextDNS

Retrieves allowlist domains for a NextDNS profile.

## Endpoint

- **Method:** `GET`
- **Path:** `/profiles/:profile/allowlist`
- **Base URL:** `https://api.nextdns.io`
- **Official documentation:** [List Allowlist](https://nextdns.io/api#nested-objects-and-arrays)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | path | `string` | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |
