# Update Profile with NextDNS

Updates an existing configuration profile in NextDNS.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/profiles/:profile`
- **Base URL:** `https://api.nextdns.io`
- **Official documentation:** [Update Profile](https://nextdns.io/api#profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | path | `string` | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |
| `name` | body | `string` | no | Profile display name. |
