# <img src="https://images.mindcloud.co/apps/icons/images-3_1775067610849.png" alt="Address Auto-Complete by Fetchify logo" width="28" height="28"> Address Auto-Complete by Fetchify: Universal API

Autocomplete and retrieve postal addresses with Fetchify's JSON Address Auto-Complete API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/addressAutoCompleteByFetchify/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fetchify.com
- **Vendor API docs:** https://docs.fetchify.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Supported Countries](actions/list-supported-countries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/addressAutoCompleteByFetchify/latest/actions/list-supported-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Find Addresses](actions/find-addresses.md) | GET | Finds address matches in Fetchify by search query. |
| [Retrieve Address](actions/retrieve-address.md) | GET | Retrieves a full address from Fetchify by address ID. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Supported Countries](actions/list-supported-countries.md) | GET | Retrieves supported address countries from Fetchify. |

