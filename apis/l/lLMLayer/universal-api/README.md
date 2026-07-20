# <img src="https://images.mindcloud.co/apps/icons/llmlayer-icon_1775764426396.png" alt="LLMLayer logo" width="28" height="28"> LLMLayer: Universal API

Web-aware AI and content extraction platform. Search the web, generate grounded answers, scrape websites, map sites, crawl pages, extract YouTube transcripts, and read PDFs through the LLMLayer API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lLMLayer/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://llmlayer.dev
- **Vendor API docs:** https://docs.llmlayer.ai/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Web](actions/search-web.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lLMLayer/latest/actions/search-web?connectionId=$CONNECTION_ID&query=Search%20query" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Answer Result

| Action | Method | Description |
| --- | --- | --- |
| [Answer in HTML](actions/answer-in-html.md) | GET | Retrieves a web-enhanced HTML answer from LLMLayer. |
| [Answer in JSON](actions/answer-in-json.md) | GET | Retrieves a web-enhanced JSON answer from LLMLayer. |
| [Answer in Markdown](actions/answer-in-markdown.md) | GET | Retrieves a web-enhanced markdown answer from LLMLayer. |
| [Answer in Spanish](actions/answer-in-spanish.md) | GET | Retrieves a Spanish web-enhanced answer from LLMLayer. |
| [Answer News Question](actions/answer-news-question.md) | GET | Retrieves a news-based answer from LLMLayer. |
| [Answer Question](actions/answer-question.md) | GET | Retrieves a web-enhanced answer from LLMLayer. |
| [Answer with Domain Filter](actions/answer-with-domain-filter.md) | GET | Retrieves a domain-filtered answer from LLMLayer. |
| [Answer with Images](actions/answer-with-images.md) | GET | Retrieves a web-enhanced answer with images from LLMLayer. |
| [Answer with Sources](actions/answer-with-sources.md) | GET | Retrieves a web-enhanced answer with sources from LLMLayer. |
| [Fast Answer](actions/fast-answer.md) | GET | Retrieves a fast web-enhanced answer from LLMLayer. |

### Crawl Result

| Action | Method | Description |
| --- | --- | --- |
| [Crawl Website](actions/crawl-website.md) | GET | Streams crawled website pages from LLMLayer. |
| [Crawl Website Deep](actions/crawl-website-deep.md) | GET | Streams deeply crawled website pages from LLMLayer. |
| [Crawl Website Main Content](actions/crawl-website-main-content.md) | GET | Streams crawled main website content from LLMLayer. |

### Map Result

| Action | Method | Description |
| --- | --- | --- |
| [Map Website URLs](actions/map-website-urls.md) | GET | Retrieves discovered website URLs from LLMLayer. |
| [Map Website with Subdomains](actions/map-website-with-subdomains.md) | GET | Retrieves discovered website and subdomain URLs from LLMLayer. |
| [Search Website URLs](actions/search-website-urls.md) | GET | Finds website URLs in LLMLayer by search term. |

### Pdf Result

| Action | Method | Description |
| --- | --- | --- |
| [Extract PDF Content](actions/extract-pdf-content.md) | GET | Retrieves extracted text from a PDF in LLMLayer. |

### Scrape Result

| Action | Method | Description |
| --- | --- | --- |
| [Capture Website Screenshot](actions/capture-website-screenshot.md) | GET | Captures a website screenshot with LLMLayer. |
| [Scrape Main Content Markdown](actions/scrape-main-content-markdown.md) | GET | Retrieves scraped main website content as markdown from LLMLayer. |
| [Scrape Rich Content](actions/scrape-rich-content.md) | GET | Retrieves scraped markdown with images and links from LLMLayer. |
| [Scrape Website HTML](actions/scrape-website-html.md) | GET | Retrieves scraped website content as HTML from LLMLayer. |
| [Scrape Website Markdown](actions/scrape-website-markdown.md) | GET | Retrieves scraped website content as markdown from LLMLayer. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Images](actions/search-images.md) | GET | Searches images in LLMLayer for raw results. |
| [Search News](actions/search-news.md) | GET | Searches news in LLMLayer for raw results. |
| [Search Scholar](actions/search-scholar.md) | GET | Searches scholarly sources in LLMLayer for raw results. |
| [Search Shopping](actions/search-shopping.md) | GET | Searches shopping in LLMLayer for raw results. |
| [Search Videos](actions/search-videos.md) | GET | Searches videos in LLMLayer for raw results. |
| [Search Web](actions/search-web.md) | GET | Searches the web in LLMLayer for raw results. |
| [Search Web with Domain Filter](actions/search-web-with-domain-filter.md) | GET | Searches the web in LLMLayer with domain filters. |

### Youtube Transcript

| Action | Method | Description |
| --- | --- | --- |
| [Get YouTube Transcript](actions/get-youtube-transcript.md) | GET | Retrieves a YouTube transcript from LLMLayer. |
| [Get YouTube Transcript by Language](actions/get-youtube-transcript-by-language.md) | GET | Retrieves a YouTube transcript by language from LLMLayer. |

