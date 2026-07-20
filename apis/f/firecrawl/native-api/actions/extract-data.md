# Extract Data with Firecrawl

Creates a data extraction job in Firecrawl.

## Endpoint

- **Method:** `POST`
- **Path:** `/extract`
- **Base URL:** `https://api.firecrawl.dev/v2`
- **Official documentation:** [Extract Data](https://docs.firecrawl.dev/api-reference/endpoint/extract)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `urls[]` | body | `array<string>` | yes | The URLs to extract data from |
| `prompt` | body | `string` | no | Prompt to guide the extraction process |
| `schema` | body | `object` | no | JSON Schema defining the structure of the extracted data |
| `enableWebSearch` | body | `boolean` | no | Use web search to find additional data |
| `ignoreSitemap` | body | `boolean` | no | Ignore sitemap.xml files during website scanning |
| `includeSubdomains` | body | `boolean` | no | Scan subdomains of the provided URLs |
| `showSources` | body | `boolean` | no | Include the sources used to extract the data |
| `scrapeOptions` | body | `object` | no | Scrape options to use during extraction |
| `ignoreInvalidURLs` | body | `boolean` | no | Ignore invalid URLs instead of failing the entire extract request |
