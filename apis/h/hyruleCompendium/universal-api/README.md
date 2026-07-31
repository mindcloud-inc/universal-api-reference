# <img src="https://images.mindcloud.co/apps/icons/api-roulette-fallback-icon_1785423907219.png" alt="Hyrule Compendium logo" width="28" height="28"> Hyrule Compendium: Universal API

Hyrule Compendium through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hyruleCompendium/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Entry](actions/get-entry.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyruleCompendium/latest/actions/get-entry?connectionId=$CONNECTION_ID&entry=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Compendium Entry

| Action | Method | Description |
| --- | --- | --- |
| [Get Entry](actions/get-entry.md) | GET |  |
| [List All Entries](actions/list-all-entries.md) | GET |  |
| [List Entries by Category](actions/list-entries-by-category.md) | GET |  |

