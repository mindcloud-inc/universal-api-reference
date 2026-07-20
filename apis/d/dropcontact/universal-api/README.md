# <img src="https://images.mindcloud.co/apps/icons/dropcontact_1774025127238.png" alt="Dropcontact logo" width="28" height="28"> Dropcontact: Universal API

Dropcontact integration for contact enrichment and webhook subscription management using API key authentication.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dropcontact/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dropcontact.com/
- **Vendor API docs:** https://developer.dropcontact.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits Left](actions/get-credits-left.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropcontact/latest/actions/get-credits-left?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Enrich Contacts](actions/enrich-contacts.md) | POST | Creates a contact enrichment request in Dropcontact. |
| [Get Credits Left](actions/get-credits-left.md) | GET | Retrieves remaining credits from Dropcontact. |
| [Get Enrichment Request](actions/get-enrichment-request.md) | GET | Retrieves contact enrichment results from Dropcontact. |

