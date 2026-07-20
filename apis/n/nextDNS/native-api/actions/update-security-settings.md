# Update Security Settings with NextDNS

Updates security settings for an existing NextDNS profile.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/profiles/:profile/security`
- **Base URL:** `https://api.nextdns.io`
- **Official documentation:** [Update Security Settings](https://nextdns.io/api#nested-objects-and-arrays)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | path | `string` | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |
| `threatIntelligenceFeeds` | body | `boolean` | no | Enable threat intelligence feeds. |
| `aiThreatDetection` | body | `boolean` | no | Enable AI threat detection. |
| `googleSafeBrowsing` | body | `boolean` | no | Enable Google Safe Browsing protection. |
| `cryptojacking` | body | `boolean` | no | Block cryptojacking threats. |
| `dnsRebinding` | body | `boolean` | no | Block DNS rebinding attacks. |
| `idnHomographs` | body | `boolean` | no | Block IDN homograph attacks. |
| `typosquatting` | body | `boolean` | no | Block typosquatting domains. |
| `dga` | body | `boolean` | no | Block domain generation algorithm domains. |
| `nrd` | body | `boolean` | no | Block newly registered domains. |
| `ddns` | body | `boolean` | no | Block dynamic DNS domains. |
| `parking` | body | `boolean` | no | Block parking domains. |
| `csam` | body | `boolean` | no | Block CSAM-related domains. |
