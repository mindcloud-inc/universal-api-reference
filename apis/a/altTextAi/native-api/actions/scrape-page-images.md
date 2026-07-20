# Scrape Page Images with AltText.Ai

Scrapes page images for alt text generation in AltText.Ai.

## Endpoint

- **Method:** `POST`
- **Path:** `/images/page_scrape`
- **Base URL:** `https://alttext.ai/api/v1`
- **Official documentation:** [Scrape Page Images](https://alttext.ai/apidocs#tag/Images/operation/page-scrape)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include_existing` | body | `boolean` | no | When true, also process images that already have alt text. |
| `keywords[]` | body | `array<string>` | no | Optional SEO keywords or phrases for generated alt text on each scraped image. |
| `lang` | body | `string` | no | One or more language codes for generated alt text. |
| `negative_keywords[]` | body | `array<string>` | no | Optional keywords or phrases to avoid in generated alt text. |
| `page_scrape` | body | `object` | yes | Provide the page URL to scrape, or raw HTML, inside this object. |
