# <img src="https://images.mindcloud.co/apps/icons/a-pi_1774871264005.png" alt="44API logo" width="28" height="28"> 44API: Universal API

Validate VAT numbers and retrieve company data across countries

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/aPI/latest
- **Category:** Commerce / Accounting
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://44api.dev
- **Vendor API docs:** https://docs.44api.dev

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate VAT Number](actions/validate-vat-number.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aPI/latest/actions/validate-vat-number?connectionId=$CONNECTION_ID&vatNumber=string&countryCode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Ip Whitelist

| Action | Method | Description |
| --- | --- | --- |
| [Manage IP Whitelist](actions/manage-ip-whitelist.md) | PUT | Manages the IP whitelist in 44API by adding, removing, or listing IPs. |

### System Status

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET | Retrieves API and upstream service status from 44API. |

### Vat Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate VAT Number](actions/validate-vat-number.md) | GET | Validates a VAT number with 44API and returns company details. |

