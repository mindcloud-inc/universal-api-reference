# <img src="https://images.mindcloud.co/apps/icons/next-dns_1776278396861.png" alt="NextDNS logo" width="28" height="28"> NextDNS: Universal API

Manage NextDNS profiles, configuration lists, analytics, and logs through the official NextDNS API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nextDNS/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://nextdns.io
- **Vendor API docs:** https://nextdns.io/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Profile](actions/get-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextDNS/latest/actions/get-profile?connectionId=$CONNECTION_ID&profileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Add Allowlist Domain](actions/add-allowlist-domain.md) | POST | Creates an allowlist domain entry in a NextDNS profile. |
| [Add Denylist Domain](actions/add-denylist-domain.md) | POST | Creates a denylist domain entry in a NextDNS profile. |
| [Clear Logs](actions/clear-logs.md) | DELETE | Deletes DNS logs from a NextDNS profile. |
| [Create Profile](actions/create-profile.md) | POST | Creates a new configuration profile in NextDNS. |
| [Delete Profile](actions/delete-profile.md) | DELETE | Deletes an existing configuration profile from NextDNS. |
| [Get Analytics Destinations by Country](actions/get-analytics-destinations-by-country.md) | GET | Retrieves destination query counts by country from NextDNS analytics. |
| [Get Analytics Devices](actions/get-analytics-devices.md) | GET | Retrieves device query counts from NextDNS analytics. |
| [Get Analytics DNSSEC](actions/get-analytics-dnssec.md) | GET | Retrieves DNSSEC validation counts from NextDNS analytics. |
| [Get Analytics Domains](actions/get-analytics-domains.md) | GET | Retrieves domain query counts from NextDNS analytics. |
| [Get Analytics Encryption](actions/get-analytics-encryption.md) | GET | Retrieves encryption query counts from NextDNS analytics. |
| [Get Analytics IP Versions](actions/get-analytics-ip-versions.md) | GET | Retrieves IP version counts from NextDNS analytics. |
| [Get Analytics IPs](actions/get-analytics-ips.md) | GET | Retrieves IP query counts from NextDNS analytics. |
| [Get Analytics Protocols](actions/get-analytics-protocols.md) | GET | Retrieves protocol query counts from NextDNS analytics. |
| [Get Analytics Query Types](actions/get-analytics-query-types.md) | GET | Retrieves query type counts from NextDNS analytics. |
| [Get Analytics Reasons](actions/get-analytics-reasons.md) | GET | Retrieves query reasons from NextDNS analytics. |
| [Get Analytics Status](actions/get-analytics-status.md) | GET | Retrieves query counts by status from NextDNS analytics. |
| [Get Logs](actions/get-logs.md) | GET | Retrieves DNS logs from a NextDNS profile. |
| [Get Parental Control](actions/get-parental-control.md) | GET | Retrieves parental control settings for a NextDNS profile. |
| [Get Performance Settings](actions/get-performance-settings.md) | GET | Retrieves performance settings for a NextDNS profile. |
| [Get Privacy Settings](actions/get-privacy-settings.md) | GET | Retrieves privacy settings for a NextDNS profile. |
| [Get Profile](actions/get-profile.md) | GET | Retrieves a configuration profile from NextDNS. |
| [Get Security Settings](actions/get-security-settings.md) | GET | Retrieves security settings for a NextDNS profile. |
| [List Allowlist](actions/list-allowlist.md) | GET | Retrieves allowlist domains for a NextDNS profile. |
| [List Denylist](actions/list-denylist.md) | GET | Retrieves denylist domains for a NextDNS profile. |
| [List Profiles](actions/list-profiles.md) | GET | Retrieves available configuration profiles from NextDNS. |
| [Update Parental Control](actions/update-parental-control.md) | PUT | Updates parental control settings for an existing NextDNS profile. |
| [Update Performance Settings](actions/update-performance-settings.md) | PUT | Updates performance settings for an existing NextDNS profile. |
| [Update Privacy Settings](actions/update-privacy-settings.md) | PUT | Updates privacy settings for an existing NextDNS profile. |
| [Update Profile](actions/update-profile.md) | PUT | Updates an existing configuration profile in NextDNS. |
| [Update Security Settings](actions/update-security-settings.md) | PUT | Updates security settings for an existing NextDNS profile. |

