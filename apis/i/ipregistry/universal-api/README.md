# <img src="https://images.mindcloud.co/apps/icons/ipregistry_1773959219621.png" alt="Ipregistry logo" width="28" height="28"> Ipregistry: Universal API

IP geolocation, threat intelligence, autonomous system, and user-agent parsing API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/ipregistry/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ipregistry.co
- **Vendor API docs:** https://ipregistry.co/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Origin IP Lookup](actions/get-origin-ip-lookup.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ipregistry/latest/actions/get-origin-ip-lookup?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Autonomous System

| Action | Method | Description |
| --- | --- | --- |
| [Get ASN Lookup](actions/get-asn-lookup.md) | GET |  |
| [Get Batch ASN Lookup](actions/get-batch-asn-lookup.md) | GET |  |
| [Get Origin ASN Lookup](actions/get-origin-asn-lookup.md) | GET |  |

### Ip Address

| Action | Method | Description |
| --- | --- | --- |
| [Get Batch IP Lookup](actions/get-batch-ip-lookup.md) | GET |  |
| [Get IP Lookup](actions/get-ip-lookup.md) | GET |  |
| [Get Origin IP Lookup](actions/get-origin-ip-lookup.md) | GET |  |

### User Agent

| Action | Method | Description |
| --- | --- | --- |
| [Parse Origin User Agent](actions/parse-origin-user-agent.md) | GET |  |
| [Parse User Agents](actions/parse-user-agents.md) | GET |  |

