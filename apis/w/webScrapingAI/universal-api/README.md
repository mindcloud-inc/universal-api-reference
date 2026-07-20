# <img src="https://images.mindcloud.co/apps/icons/web-scraping-ai_1774023475674.png" alt="WebScraping.AI logo" width="28" height="28"> WebScraping.AI: Universal API

Extract website HTML, text, and structured data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/webScrapingAI/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://webscraping.ai
- **Vendor API docs:** https://webscraping.ai/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Page HTML](actions/get-page-html.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webScrapingAI/latest/actions/get-page-html?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Page Answer

| Action | Method | Description |
| --- | --- | --- |
| [Ask Questions About a Page](actions/ask-questions-about-a-page.md) | GET |  |

### Page Html

| Action | Method | Description |
| --- | --- | --- |
| [Get Page HTML](actions/get-page-html.md) | GET |  |

### Page Text

| Action | Method | Description |
| --- | --- | --- |
| [Get Page Text](actions/get-page-text.md) | GET |  |

### Selected Html

| Action | Method | Description |
| --- | --- | --- |
| [Get Selected HTML](actions/get-selected-html.md) | GET |  |

### Selected Html Fragments

| Action | Method | Description |
| --- | --- | --- |
| [Get Selected HTML For Multiple Selectors](actions/get-selected-html-for-multiple-selectors.md) | GET |  |

### Structured Fields

| Action | Method | Description |
| --- | --- | --- |
| [Extract Structured Fields](actions/extract-structured-fields.md) | GET |  |

