# NextDNS: Native API Reference

A consolidated summary of NextDNS's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://nextdns.io/api
- **API base URL:** `https://api.nextdns.io`

## Authentication

### API Key

Authenticate with a NextDNS API key. Add the default profile ID separately for profile-scoped actions.

### Credentials

- **API Key:** `apiKey` · required
- **Profile ID:** `profileId` · required · Default NextDNS profile identifier used by profile-scoped actions, for example 8c8588.

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://nextdns.io/api)

## API conventions

Response data is read from `data`. The next-page cursor is read from `meta.pagination.cursor`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–500). Use `cursor` in the query string as the pagination cursor.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Allowlist Domain](actions/add-allowlist-domain.md) | `POST /profiles/:profile/allowlist` | [docs](https://nextdns.io/api#nested-objects-and-arrays) |
| [Add Denylist Domain](actions/add-denylist-domain.md) | `POST /profiles/:profile/denylist` | [docs](https://nextdns.io/api#nested-objects-and-arrays) |
| [Clear Logs](actions/clear-logs.md) | `DELETE /profiles/:profile/logs` | [docs](https://nextdns.io/api#clear) |
| [Create Profile](actions/create-profile.md) | `POST /profiles` | [docs](https://nextdns.io/api#profile) |
| [Delete Profile](actions/delete-profile.md) | `DELETE /profiles/:profile` | [docs](https://nextdns.io/api#profile) |
| [Get Analytics Destinations by Country](actions/get-analytics-destinations-by-country.md) | `GET /profiles/:profile/analytics/destinations` | [docs](https://nextdns.io/api#profilesprofileanalyticsdestinationstypecountries) |
| [Get Analytics Devices](actions/get-analytics-devices.md) | `GET /profiles/:profile/analytics/devices` | [docs](https://nextdns.io/api#profilesprofileanalyticsdevices) |
| [Get Analytics DNSSEC](actions/get-analytics-dnssec.md) | `GET /profiles/:profile/analytics/dnssec` | [docs](https://nextdns.io/api#profilesprofileanalyticsdnssec) |
| [Get Analytics Domains](actions/get-analytics-domains.md) | `GET /profiles/:profile/analytics/domains` | [docs](https://nextdns.io/api#profilesprofileanalyticsdomains) |
| [Get Analytics Encryption](actions/get-analytics-encryption.md) | `GET /profiles/:profile/analytics/encryption` | [docs](https://nextdns.io/api#profilesprofileanalyticsencryption) |
| [Get Analytics IP Versions](actions/get-analytics-ip-versions.md) | `GET /profiles/:profile/analytics/ipVersions` | [docs](https://nextdns.io/api#profilesprofileanalyticsipversions) |
| [Get Analytics IPs](actions/get-analytics-ips.md) | `GET /profiles/:profile/analytics/ips` | [docs](https://nextdns.io/api#profilesprofileanalyticsips) |
| [Get Analytics Protocols](actions/get-analytics-protocols.md) | `GET /profiles/:profile/analytics/protocols` | [docs](https://nextdns.io/api#profilesprofileanalyticsprotocols) |
| [Get Analytics Query Types](actions/get-analytics-query-types.md) | `GET /profiles/:profile/analytics/queryTypes` | [docs](https://nextdns.io/api#profilesprofileanalyticsquerytypes) |
| [Get Analytics Reasons](actions/get-analytics-reasons.md) | `GET /profiles/:profile/analytics/reasons` | [docs](https://nextdns.io/api#profilesprofileanalyticsreasons) |
| [Get Analytics Status](actions/get-analytics-status.md) | `GET /profiles/:profile/analytics/status` | [docs](https://nextdns.io/api#profilesprofileanalyticsstatus) |
| [Get Logs](actions/get-logs.md) | `GET /profiles/:profile/logs` | [docs](https://nextdns.io/api#logs) |
| [Get Parental Control](actions/get-parental-control.md) | `GET /profiles/:profile/parentalControl` | [docs](https://nextdns.io/api#nested-objects-and-arrays) |
| [Get Performance Settings](actions/get-performance-settings.md) | `GET /profiles/:profile/settings/performance` | [docs](https://nextdns.io/api#nested-objects-and-arrays) |
| [Get Privacy Settings](actions/get-privacy-settings.md) | `GET /profiles/:profile/privacy` | [docs](https://nextdns.io/api#nested-objects-and-arrays) |
| [Get Profile](actions/get-profile.md) | `GET /profiles/:profile` | [docs](https://nextdns.io/api#profile) |
| [Get Security Settings](actions/get-security-settings.md) | `GET /profiles/:profile/security` | [docs](https://nextdns.io/api#nested-objects-and-arrays) |
| [List Allowlist](actions/list-allowlist.md) | `GET /profiles/:profile/allowlist` | [docs](https://nextdns.io/api#nested-objects-and-arrays) |
| [List Denylist](actions/list-denylist.md) | `GET /profiles/:profile/denylist` | [docs](https://nextdns.io/api#nested-objects-and-arrays) |
| [List Profiles](actions/list-profiles.md) | `GET /profiles` | [docs](https://nextdns.io/api#profiles) |
| [Update Parental Control](actions/update-parental-control.md) | `PATCH /profiles/:profile/parentalControl` | [docs](https://nextdns.io/api#nested-objects-and-arrays) |
| [Update Performance Settings](actions/update-performance-settings.md) | `PATCH /profiles/:profile/settings/performance` | [docs](https://nextdns.io/api#nested-objects-and-arrays) |
| [Update Privacy Settings](actions/update-privacy-settings.md) | `PATCH /profiles/:profile/privacy` | [docs](https://nextdns.io/api#nested-objects-and-arrays) |
| [Update Profile](actions/update-profile.md) | `PATCH /profiles/:profile` | [docs](https://nextdns.io/api#profile) |
| [Update Security Settings](actions/update-security-settings.md) | `PATCH /profiles/:profile/security` | [docs](https://nextdns.io/api#nested-objects-and-arrays) |
