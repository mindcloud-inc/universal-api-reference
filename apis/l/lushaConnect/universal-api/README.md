# <img src="https://images.mindcloud.co/apps/icons/lusha-connect_1773950641601.png" alt="Lusha Connect logo" width="28" height="28"> Lusha Connect: Universal API

Search, enrich, and monitor contacts and companies with the official Lusha API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lushaConnect/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lusha.com
- **Vendor API docs:** https://docs.lusha.com/apis/openapi

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Usage](actions/get-account-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lushaConnect/latest/actions/get-account-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in Lusha Connect by enrichment inputs. |
| [Search Prospecting Companies](actions/search-prospecting-companies.md) | GET | Finds prospecting companies in Lusha Connect by filters. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contacts in Lusha Connect by enrichment inputs. |
| [Search Prospecting Contacts](actions/search-prospecting-contacts.md) | GET | Finds prospecting contacts in Lusha Connect by filters. |

### Service Accounts

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Usage](actions/get-account-usage.md) | GET | Retrieves account usage statistics from Lusha Connect. |

