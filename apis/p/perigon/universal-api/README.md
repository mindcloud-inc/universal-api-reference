# <img src="https://images.mindcloud.co/apps/icons/images-2_1775752891477.png" alt="Perigon logo" width="28" height="28"> Perigon: Universal API

Perigon is a news intelligence API for searching articles, stories, sources, journalists, people, companies, topics, summaries, and Wikipedia content.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/perigon/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.perigon.io
- **Vendor API docs:** https://docs.perigon.io/docs/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Articles](actions/search-articles.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/perigon/latest/actions/search-articles?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Articles

| Action | Method | Description |
| --- | --- | --- |
| [Search Articles](actions/search-articles.md) | GET | Finds news articles in Perigon by keywords and filters. |
| [Vector Search Articles](actions/vector-search-articles.md) | GET | Finds Perigon articles by semantic similarity to a prompt. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in Perigon by name, symbol, or domain. |

### Journalists

| Action | Method | Description |
| --- | --- | --- |
| [Get Journalist By ID](actions/get-journalist-by-id.md) | GET | Retrieves a journalist profile from Perigon by ID. |
| [Search Journalists](actions/search-journalists.md) | GET | Finds journalists in Perigon by name, source, or topic. |

### People

| Action | Method | Description |
| --- | --- | --- |
| [Search People](actions/search-people.md) | GET | Finds people in Perigon by name or Wikidata details. |

### Sources

| Action | Method | Description |
| --- | --- | --- |
| [Search Sources](actions/search-sources.md) | GET | Finds media sources in Perigon by attributes and filters. |

### Stories

| Action | Method | Description |
| --- | --- | --- |
| [Get Story Counts](actions/get-story-counts.md) | GET | Retrieves Perigon story counts grouped by filters or dimensions. |
| [Get Story History](actions/get-story-history.md) | GET | Retrieves historical changes for Perigon stories over time. |
| [Search Stories](actions/search-stories.md) | GET | Finds clustered news stories in Perigon by keywords and filters. |

### Summaries

| Action | Method | Description |
| --- | --- | --- |
| [Search Summarizer](actions/search-summarizer.md) | GET | Generates Perigon news summaries from a custom prompt. |

### Topics

| Action | Method | Description |
| --- | --- | --- |
| [Search Topics](actions/search-topics.md) | GET | Finds topics in Perigon by name or category. |

### Wikipedia

| Action | Method | Description |
| --- | --- | --- |
| [Search Wikipedia](actions/search-wikipedia.md) | GET | Finds Wikipedia pages through Perigon by text or metadata. |
| [Vector Search Wikipedia](actions/vector-search-wikipedia.md) | GET | Finds Wikipedia pages by semantic similarity through Perigon. |

