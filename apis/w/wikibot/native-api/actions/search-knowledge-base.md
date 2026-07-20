# Search Knowledge Base with Wikibot

Finds knowledge base articles in Wikibot by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/bot/search`
- **Base URL:** `https://api.wikibot.pro/api`
- **Official documentation:** [Search Knowledge Base](https://wikibot.pro/docs/api/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | yes | Search query. |
| `skip` | query | `string` | no | Number of records to skip. |
| `take` | query | `string` | no | Number of records to return. |
