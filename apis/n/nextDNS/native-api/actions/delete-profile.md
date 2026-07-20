# Delete Profile with NextDNS

Deletes an existing configuration profile from NextDNS.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/profiles/:profile`
- **Base URL:** `https://api.nextdns.io`
- **Official documentation:** [Delete Profile](https://nextdns.io/api#profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | path | `string` | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |
