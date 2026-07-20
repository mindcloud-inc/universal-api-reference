# <img src="https://images.mindcloud.co/apps/icons/dandelion_1775059423606.png" alt="Dandelion logo" width="28" height="28"> Dandelion: Universal API

Dandelion: Analyze text for language, entities, sentiment, similarity, and Wikipedia matches

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dandelion/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dandelion.eu
- **Vendor API docs:** https://dandelion.eu/docs/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Detect Language From Text via HTTP GET](actions/detect-language-from-text-get.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/detect-language-from-text-get?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Entity Annotation

| Action | Method | Description |
| --- | --- | --- |
| [Extract Entities From HTML Fragment via HTTP GET](actions/extract-entities-from-html-fragment-get.md) | GET | Retrieves entities from an HTML fragment in Dandelion via HTTP GET. |
| [Extract Entities From HTML Fragment via HTTP POST](actions/extract-entities-from-html-fragment-post.md) | GET | Retrieves entities from an HTML fragment in Dandelion via HTTP POST. |
| [Extract Entities From HTML via HTTP GET](actions/extract-entities-from-html-get.md) | GET | Retrieves entities from HTML in Dandelion via HTTP GET. |
| [Extract Entities From HTML via HTTP POST](actions/extract-entities-from-html-post.md) | GET | Retrieves entities from HTML in Dandelion via HTTP POST. |
| [Extract Entities From Text via HTTP GET](actions/extract-entities-from-text-get.md) | GET | Retrieves entities from text in Dandelion via HTTP GET. |
| [Extract Entities From Text via HTTP POST](actions/extract-entities-from-text-post.md) | GET | Retrieves entities from text in Dandelion via HTTP POST. |

### Language Detection

| Action | Method | Description |
| --- | --- | --- |
| [Detect Language From HTML Fragment via HTTP GET](actions/detect-language-from-html-fragment-get.md) | GET | Retrieves detected languages from an HTML fragment in Dandelion via HTTP GET. |
| [Detect Language From HTML Fragment via HTTP POST](actions/detect-language-from-html-fragment-post.md) | GET | Retrieves detected languages from an HTML fragment in Dandelion via HTTP POST. |
| [Detect Language From HTML via HTTP GET](actions/detect-language-from-html-get.md) | GET | Retrieves detected languages from HTML in Dandelion via HTTP GET. |
| [Detect Language From HTML via HTTP POST](actions/detect-language-from-html-post.md) | GET | Retrieves detected languages from HTML in Dandelion via HTTP POST. |
| [Detect Language From Text via HTTP GET](actions/detect-language-from-text-get.md) | GET | Retrieves detected languages from text in Dandelion via HTTP GET. |
| [Detect Language From Text via HTTP POST](actions/detect-language-from-text-post.md) | GET | Retrieves detected languages from text in Dandelion via HTTP POST. |

### Sentiment Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Sentiment From HTML Fragment via HTTP GET](actions/analyze-sentiment-from-html-fragment-get.md) | GET | Retrieves sentiment from an HTML fragment in Dandelion via HTTP GET. |
| [Analyze Sentiment From HTML Fragment via HTTP POST](actions/analyze-sentiment-from-html-fragment-post.md) | GET | Retrieves sentiment from an HTML fragment in Dandelion via HTTP POST. |
| [Analyze Sentiment From HTML via HTTP GET](actions/analyze-sentiment-from-html-get.md) | GET | Retrieves sentiment from HTML in Dandelion via HTTP GET. |
| [Analyze Sentiment From HTML via HTTP POST](actions/analyze-sentiment-from-html-post.md) | GET | Retrieves sentiment from HTML in Dandelion via HTTP POST. |
| [Analyze Sentiment From Text via HTTP GET](actions/analyze-sentiment-from-text-get.md) | GET | Retrieves sentiment from text in Dandelion via HTTP GET. |
| [Analyze Sentiment From Text via HTTP POST](actions/analyze-sentiment-from-text-post.md) | GET | Retrieves sentiment from text in Dandelion via HTTP POST. |

### Text Similarity

| Action | Method | Description |
| --- | --- | --- |
| [Compare HTML Fragment Similarity via HTTP GET](actions/compare-html-fragment-similarity-get.md) | GET | Retrieves HTML fragment similarity from Dandelion via HTTP GET. |
| [Compare HTML Fragment Similarity via HTTP POST](actions/compare-html-fragment-similarity-post.md) | GET | Retrieves HTML fragment similarity from Dandelion via HTTP POST. |
| [Compare HTML Similarity via HTTP GET](actions/compare-html-similarity-get.md) | GET | Retrieves HTML similarity from Dandelion via HTTP GET. |
| [Compare HTML Similarity via HTTP POST](actions/compare-html-similarity-post.md) | GET | Retrieves HTML similarity from Dandelion via HTTP POST. |
| [Compare Text Similarity via HTTP GET](actions/compare-text-similarity-get.md) | GET | Retrieves text similarity from Dandelion via HTTP GET. |
| [Compare Text Similarity via HTTP POST](actions/compare-text-similarity-post.md) | GET | Retrieves text similarity from Dandelion via HTTP POST. |

### Wikipedia Entity

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Wikipedia Entities via HTTP GET](actions/autocomplete-wikipedia-entities-get.md) | GET | Autocompletes Wikipedia entities in Dandelion via HTTP GET. |
| [Autocomplete Wikipedia Entities via HTTP POST](actions/autocomplete-wikipedia-entities-post.md) | GET | Autocompletes Wikipedia entities in Dandelion via HTTP POST. |
| [Search Wikipedia Entities via HTTP GET](actions/search-wikipedia-entities-get.md) | GET | Searches Wikipedia entities in Dandelion via HTTP GET. |
| [Search Wikipedia Entities via HTTP POST](actions/search-wikipedia-entities-post.md) | GET | Searches Wikipedia entities in Dandelion via HTTP POST. |

