# <img src="https://images.mindcloud.co/apps/icons/sandbox_1776256325807.png" alt="Sandbox logo" width="28" height="28"> Sandbox: Universal API

Verify tax IDs, fetch GST records, and run KYC workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sandbox/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://sandbox.co.in
- **Vendor API docs:** https://developer.sandbox.co.in/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search GSTIN](actions/search-gstin.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sandbox/latest/actions/search-gstin?connectionId=$CONNECTION_ID&gstin=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Authenticate](actions/authenticate.md) | GET | Retrieves a JWT access token from Sandbox. |
| [Search GSTIN](actions/search-gstin.md) | GET | Retrieves GST registration details from Sandbox by GSTIN. |

