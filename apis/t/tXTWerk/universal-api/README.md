# <img src="https://images.mindcloud.co/apps/icons/t-xtwerk_1776269890423.png" alt="TXT Werk logo" width="28" height="28"> TXT Werk: Universal API

Analyze text for entities, tags, categories, dates, and measures

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/tXTWerk/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ontolux.de
- **Vendor API docs:** https://services.txtwerk.de/ws/documentation/index

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Analyze Text](actions/analyze-text.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tXTWerk/latest/actions/analyze-text?connectionId=$CONNECTION_ID&text=string&services=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Annotated Entities](actions/analyze-annotated-entities.md) | GET | Retrieves annotated entities from text in TXT Werk. |
| [Analyze Entity Candidates](actions/analyze-entity-candidates.md) | GET | Retrieves entity candidates from text in TXT Werk. |
| [Analyze HTML Article Authors](actions/analyze-html-article-authors.md) | GET | Retrieves article authors from HTML in TXT Werk. |
| [Analyze HTML Article Bundle](actions/analyze-html-article-bundle.md) | GET | Analyzes an HTML article bundle in TXT Werk. |
| [Analyze Metadata-Enriched Entities](actions/analyze-metadata-enriched-entities.md) | GET | Retrieves metadata-enriched entities from text in TXT Werk. |
| [Analyze Named Entities](actions/analyze-named-entities.md) | GET | Retrieves named entities from text in TXT Werk. |
| [Analyze Text](actions/analyze-text.md) | GET | Analyzes text content in TXT Werk. |
| [Analyze Top Entities](actions/analyze-top-entities.md) | GET | Retrieves top entities from text in TXT Werk. |
| [Analyze Weighted Document Bundle](actions/analyze-weighted-document-bundle.md) | GET | Analyzes a weighted document bundle in TXT Werk. |
| [Classify Categories](actions/classify-categories.md) | GET | Retrieves categories from text in TXT Werk. |
| [Extract Dates](actions/extract-dates.md) | GET | Retrieves dates from text in TXT Werk. |
| [Extract Lexicon Entities](actions/extract-lexicon-entities.md) | GET | Retrieves lexicon entities from text in TXT Werk. |
| [Extract Lexicon Tags](actions/extract-lexicon-tags.md) | GET | Retrieves lexicon tags from text in TXT Werk. |
| [Extract Measures](actions/extract-measures.md) | GET | Retrieves measures from text in TXT Werk. |
| [Extract NER Entities](actions/extract-ner-entities.md) | GET | Retrieves NER entities from text in TXT Werk. |
| [Extract Tags](actions/extract-tags.md) | GET | Retrieves tags from text in TXT Werk. |
| [Extract Tags With Title And Teaser](actions/extract-tags-with-title-and-teaser.md) | GET | Retrieves tags from text using title and teaser in TXT Werk. |
| [Generate Fingerprints](actions/generate-fingerprints.md) | GET | Generates document fingerprints from text in TXT Werk. |

