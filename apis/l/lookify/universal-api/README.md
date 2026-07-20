# <img src="https://images.mindcloud.co/apps/icons/lookify_1774987662183.png" alt="Lookify logo" width="28" height="28"> Lookify: Universal API

Lookify provides an enterprise carrier lookup API for retrieving carrier information for a phone number.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lookify/latest
- **Category:** IT Operations / Security & Identity
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lookify.io
- **Vendor API docs:** https://lookify.io/assets/pdfs/enterprise_carrier_api_documentation.pdf

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Lookup Carrier](actions/lookup-carrier.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lookify/latest/actions/lookup-carrier?connectionId=$CONNECTION_ID&nid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Carrier Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Carrier](actions/lookup-carrier.md) | GET |  |

