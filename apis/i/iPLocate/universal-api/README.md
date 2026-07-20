# <img src="https://images.mindcloud.co/apps/icons/i-plocate_1775828216830.png" alt="IPLocate logo" width="28" height="28"> IPLocate: Universal API

IPLocate provides IP geolocation and intelligence lookups, including country, city, ASN, privacy, company, hosting, abuse, and historical IP data.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iPLocate/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 32
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.iplocate.io
- **Vendor API docs:** https://www.iplocate.io/docs/ip-intelligence-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Lookup Current IP](actions/lookup-current-ip.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPLocate/latest/actions/lookup-current-ip?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (32)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Company](actions/lookup-company.md) | GET |  |
| [Lookup Company Name](actions/lookup-company-name.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Abuse Contact](actions/lookup-abuse-contact.md) | GET |  |
| [Lookup Abuse Email](actions/lookup-abuse-email.md) | GET |  |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Batch Lookup](actions/batch-lookup.md) | GET |  |
| [Lookup Anonymous Status](actions/lookup-anonymous-status.md) | GET |  |
| [Lookup ASN](actions/lookup-asn.md) | GET |  |
| [Lookup ASN Number](actions/lookup-asn-number.md) | GET |  |
| [Lookup ASN Route](actions/lookup-asn-route.md) | GET |  |
| [Lookup Bogon Status](actions/lookup-bogon-status.md) | GET |  |
| [Lookup Calling Code](actions/lookup-calling-code.md) | GET |  |
| [Lookup City](actions/lookup-city.md) | GET |  |
| [Lookup Continent](actions/lookup-continent.md) | GET |  |
| [Lookup Coordinates](actions/lookup-coordinates.md) | GET |  |
| [Lookup Country](actions/lookup-country.md) | GET |  |
| [Lookup Country Code](actions/lookup-country-code.md) | GET |  |
| [Lookup Currency Code](actions/lookup-currency-code.md) | GET |  |
| [Lookup Current IP](actions/lookup-current-ip.md) | GET |  |
| [Lookup Current IP Custom Fields](actions/lookup-current-ip-custom-fields.md) | GET |  |
| [Lookup Custom Fields](actions/lookup-custom-fields.md) | GET |  |
| [Lookup Historical IP](actions/lookup-historical-ip.md) | GET |  |
| [Lookup Hosting](actions/lookup-hosting.md) | GET |  |
| [Lookup Hosting Provider](actions/lookup-hosting-provider.md) | GET |  |
| [Lookup Hosting Status](actions/lookup-hosting-status.md) | GET |  |
| [Lookup IP](actions/lookup-ip.md) | GET |  |
| [Lookup Postal Code](actions/lookup-postal-code.md) | GET |  |
| [Lookup Privacy](actions/lookup-privacy.md) | GET |  |
| [Lookup Proxy Status](actions/lookup-proxy-status.md) | GET |  |
| [Lookup Subdivision](actions/lookup-subdivision.md) | GET |  |
| [Lookup Time Zone](actions/lookup-time-zone.md) | GET |  |
| [Lookup Tor Status](actions/lookup-tor-status.md) | GET |  |
| [Lookup VPN Status](actions/lookup-vpn-status.md) | GET |  |

