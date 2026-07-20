# <img src="https://images.mindcloud.co/apps/icons/ipdataco_1776184741463.png" alt="ipdata.co logo" width="28" height="28"> ipdata.co: Universal API

Look up IP geolocation, ownership, and threat intelligence

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ipdataco/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ipdata.co
- **Vendor API docs:** https://docs.ipdata.co

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get IP Details](actions/get-ip-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ipdataco/latest/actions/get-ip-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Blocklists

| Action | Method | Description |
| --- | --- | --- |
| [Get IP Blocklists](actions/get-ip-blocklists.md) | GET |  |

### Carrier

| Action | Method | Description |
| --- | --- | --- |
| [Get Caller IP Carrier](actions/get-caller-ip-carrier.md) | GET |  |
| [Get IP Carrier](actions/get-ip-carrier.md) | GET |  |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Caller IP Company](actions/get-caller-ip-company.md) | GET |  |
| [Get IP Company](actions/get-ip-company.md) | GET |  |

### Location

| Action | Method | Description |
| --- | --- | --- |
| [Get Caller IP Basic ASN](actions/get-caller-ip-basic-asn.md) | GET |  |
| [Get Caller IP Coordinates](actions/get-caller-ip-coordinates.md) | GET |  |
| [Get Caller IP Country](actions/get-caller-ip-country.md) | GET |  |
| [Get Caller IP Country Metadata](actions/get-caller-ip-country-metadata.md) | GET |  |
| [Get Caller IP Currency](actions/get-caller-ip-currency.md) | GET |  |
| [Get Caller IP Details](actions/get-caller-ip-details.md) | GET |  |
| [Get Caller IP Languages](actions/get-caller-ip-languages.md) | GET |  |
| [Get Caller IP Region And Postal](actions/get-caller-ip-region-and-postal.md) | GET |  |
| [Get Caller IP Selected Fields](actions/get-caller-ip-selected-fields.md) | GET |  |
| [Get Caller IP Time Zone](actions/get-caller-ip-time-zone.md) | GET |  |
| [Get IP Basic ASN](actions/get-ip-basic-asn.md) | GET |  |
| [Get IP Coordinates](actions/get-ip-coordinates.md) | GET |  |
| [Get IP Country](actions/get-ip-country.md) | GET |  |
| [Get IP Country Metadata](actions/get-ip-country-metadata.md) | GET |  |
| [Get IP Currency](actions/get-ip-currency.md) | GET |  |
| [Get IP Details](actions/get-ip-details.md) | GET |  |
| [Get IP Languages](actions/get-ip-languages.md) | GET |  |
| [Get IP Region And Postal](actions/get-ip-region-and-postal.md) | GET |  |
| [Get IP Selected Fields](actions/get-ip-selected-fields.md) | GET |  |
| [Get IP Time Zone](actions/get-ip-time-zone.md) | GET |  |

### Reputation Scores

| Action | Method | Description |
| --- | --- | --- |
| [Get IP Reputation Scores](actions/get-ip-reputation-scores.md) | GET |  |

### Threat Summary

| Action | Method | Description |
| --- | --- | --- |
| [Get Caller IP Threat Summary](actions/get-caller-ip-threat-summary.md) | GET |  |
| [Get IP Threat Summary](actions/get-ip-threat-summary.md) | GET |  |

### Vpn Detection

| Action | Method | Description |
| --- | --- | --- |
| [Get IP VPN Detection](actions/get-ipvpn-detection.md) | GET |  |

