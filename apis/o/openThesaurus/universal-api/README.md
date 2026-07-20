# <img src="https://images.mindcloud.co/apps/icons/open-thesaurus_1775768286334.png" alt="OpenThesaurus logo" width="28" height="28"> OpenThesaurus: Universal API

Public OpenThesaurus synonym search API. Requests must include a contactable User-Agent and the app should preserve a visible link to openthesaurus.de because the service is rate-limited and asks users to identify themselves.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openThesaurus/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.openthesaurus.de/
- **Vendor API docs:** https://www.openthesaurus.de/about/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Synonyms](actions/search-synonyms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openThesaurus/latest/actions/search-synonyms?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (1)

### Synonym Group

| Action | Method | Description |
| --- | --- | --- |
| [Search Synonyms](actions/search-synonyms.md) | GET |  |

