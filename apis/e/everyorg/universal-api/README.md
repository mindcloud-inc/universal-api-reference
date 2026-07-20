# <img src="https://images.mindcloud.co/apps/icons/everyorg_1774466295338.png" alt="Every.org logo" width="28" height="28"> Every.org: Universal API

Search nonprofits and create fundraisers with Every.org

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/everyorg/latest
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.every.org/charity-api
- **Vendor API docs:** https://docs.every.org/docs/intro

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Nonprofit](actions/get-nonprofit.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everyorg/latest/actions/get-nonprofit?connectionId=$CONNECTION_ID&identifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Fundraiser

| Action | Method | Description |
| --- | --- | --- |
| [Create Fundraiser](actions/create-fundraiser.md) | POST | Creates a new fundraiser in Every.org. |
| [Get Fundraiser](actions/get-fundraiser.md) | GET | Retrieves details about a fundraiser from Every.org. |
| [Get Fundraiser Raised](actions/get-fundraiser-raised.md) | GET | Retrieves raised totals for a fundraiser from Every.org. |

### Nonprofit

| Action | Method | Description |
| --- | --- | --- |
| [Browse Nonprofits](actions/browse-nonprofits.md) | GET | Finds nonprofits in Every.org by cause. |
| [Get Nonprofit](actions/get-nonprofit.md) | GET | Retrieves details about a nonprofit from Every.org. |
| [Search Nonprofits](actions/search-nonprofits.md) | GET | Finds nonprofits in Every.org by search term. |

