# Update Privacy Settings with NextDNS

Updates privacy settings for an existing NextDNS profile.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/profiles/:profile/privacy`
- **Base URL:** `https://api.nextdns.io`
- **Official documentation:** [Update Privacy Settings](https://nextdns.io/api#nested-objects-and-arrays)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | path | `string` | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |
| `disguisedTrackers` | body | `boolean` | no | Toggle disguised third-party trackers blocking. |
| `allowAffiliate` | body | `boolean` | no | Allow affiliate links. |
