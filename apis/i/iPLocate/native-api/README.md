# IPLocate: Native API Reference

A consolidated summary of IPLocate's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://www.iplocate.io/docs/ip-intelligence-api/
- **API base URL:** `https://iplocate.io/api`

## Authentication

### IPLocate API Key

Custom auth for IPLocate requests that send the tenant API key using the provider's supported non-bearer contract.

### Credentials

- **API Key:** `apiKey` · required · Enter your IPLocate API key.

[Official authentication documentation](https://www.iplocate.io/docs/getting-started/authentication)

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Batch Lookup](actions/batch-lookup.md) | `POST /batch` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/batch-lookup) |
| [Lookup Abuse Contact](actions/lookup-abuse-contact.md) | `GET /lookup/:ip/abuse` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Abuse Email](actions/lookup-abuse-email.md) | `GET /lookup/:ip/abuse.email` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Anonymous Status](actions/lookup-anonymous-status.md) | `GET /lookup/:ip/privacy.is_anonymous` | [docs](https://www.iplocate.io/docs/guides/detect-vpn-and-proxies) |
| [Lookup ASN](actions/lookup-asn.md) | `GET /lookup/:ip/asn` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup ASN Number](actions/lookup-asn-number.md) | `GET /lookup/:ip/asn.asn` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup ASN Route](actions/lookup-asn-route.md) | `GET /lookup/:ip/asn.route` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Bogon Status](actions/lookup-bogon-status.md) | `GET /lookup/:ip/privacy.is_bogon` | [docs](https://www.iplocate.io/docs/guides/bogons) |
| [Lookup Calling Code](actions/lookup-calling-code.md) | `GET /lookup/:ip/calling_code` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup City](actions/lookup-city.md) | `GET /lookup/:ip/city` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Company](actions/lookup-company.md) | `GET /lookup/:ip/company` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Company Name](actions/lookup-company-name.md) | `GET /lookup/:ip/company.name` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Continent](actions/lookup-continent.md) | `GET /lookup/:ip/continent` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Coordinates](actions/lookup-coordinates.md) | `GET /lookup/:ip` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Country](actions/lookup-country.md) | `GET /lookup/:ip/country` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Country Code](actions/lookup-country-code.md) | `GET /lookup/:ip/country_code` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Currency Code](actions/lookup-currency-code.md) | `GET /lookup/:ip/currency_code` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Current IP](actions/lookup-current-ip.md) | `GET /lookup/` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Current IP Custom Fields](actions/lookup-current-ip-custom-fields.md) | `GET /lookup/` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Custom Fields](actions/lookup-custom-fields.md) | `GET /lookup/:ip` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Historical IP](actions/lookup-historical-ip.md) | `GET /lookup/:ip` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/historical-lookup) |
| [Lookup Hosting](actions/lookup-hosting.md) | `GET /lookup/:ip/hosting` | [docs](https://www.iplocate.io/docs/guides/detect-hosting-traffic) |
| [Lookup Hosting Provider](actions/lookup-hosting-provider.md) | `GET /lookup/:ip/hosting.provider` | [docs](https://www.iplocate.io/docs/guides/detect-hosting-traffic) |
| [Lookup Hosting Status](actions/lookup-hosting-status.md) | `GET /lookup/:ip/privacy.is_hosting` | [docs](https://www.iplocate.io/docs/guides/detect-hosting-traffic) |
| [Lookup IP](actions/lookup-ip.md) | `GET /lookup/:ip` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Postal Code](actions/lookup-postal-code.md) | `GET /lookup/:ip/postal_code` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Privacy](actions/lookup-privacy.md) | `GET /lookup/:ip/privacy` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Proxy Status](actions/lookup-proxy-status.md) | `GET /lookup/:ip/privacy.is_proxy` | [docs](https://www.iplocate.io/docs/guides/detect-vpn-and-proxies) |
| [Lookup Subdivision](actions/lookup-subdivision.md) | `GET /lookup/:ip/subdivision` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Time Zone](actions/lookup-time-zone.md) | `GET /lookup/:ip/time_zone` | [docs](https://www.iplocate.io/docs/ip-intelligence-api/) |
| [Lookup Tor Status](actions/lookup-tor-status.md) | `GET /lookup/:ip/privacy.is_tor` | [docs](https://www.iplocate.io/docs/guides/detect-vpn-and-proxies) |
| [Lookup VPN Status](actions/lookup-vpn-status.md) | `GET /lookup/:ip/privacy.is_vpn` | [docs](https://www.iplocate.io/docs/guides/detect-vpn-and-proxies) |
