# Get Profile with NextDNS

Retrieves a configuration profile from NextDNS.

## Endpoint

- **Method:** `GET`
- **Path:** `/profiles/:profile`
- **Base URL:** `https://api.nextdns.io`
- **Official documentation:** [Get Profile](https://nextdns.io/api#profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | path | `string` | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |
