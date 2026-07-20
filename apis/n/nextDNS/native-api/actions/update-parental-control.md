# Update Parental Control with NextDNS

Updates parental control settings for an existing NextDNS profile.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/profiles/:profile/parentalControl`
- **Base URL:** `https://api.nextdns.io`
- **Official documentation:** [Update Parental Control](https://nextdns.io/api#nested-objects-and-arrays)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | path | `string` | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |
| `safeSearch` | body | `boolean` | no | Toggle safe search. |
| `youtubeRestrictedMode` | body | `boolean` | no | Toggle YouTube restricted mode. |
| `blockBypass` | body | `boolean` | no | Toggle block bypass protection. |
