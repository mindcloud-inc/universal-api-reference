# <img src="https://images.mindcloud.co/apps/icons/wiza_1773941771434.png" alt="Wiza logo" width="28" height="28"> Wiza: Universal API

Find and verify contact information for sales and recruiting prospects

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/wiza/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://wiza.co
- **Vendor API docs:** https://docs.wiza.co

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiza/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Company Enrichment](actions/company-enrichment.md) | GET | Retrieves enriched company data from Wiza. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Individual Reveal](actions/get-individual-reveal.md) | GET | Retrieves an individual reveal from Wiza. |
| [Get List Contacts](actions/get-list-contacts.md) | GET | Retrieves contacts for a Wiza list. |
| [Prospect Search](actions/prospect-search.md) | GET | Finds the number of matching prospects in Wiza. |
| [Start Individual Reveal](actions/start-individual-reveal.md) | POST | Starts an individual reveal in Wiza. |

### Credits

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET | Retrieves your remaining Wiza credits. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Continue Prospect Search](actions/continue-prospect-search.md) | POST | Continues a previous prospect search in Wiza. |
| [Create List](actions/create-list.md) | POST | Creates a Wiza list of people to enrich. |
| [Create Prospect List](actions/create-prospect-list.md) | POST | Creates a Wiza prospect list from filters. |
| [Get List](actions/get-list.md) | GET | Retrieves a Wiza list by ID. |

