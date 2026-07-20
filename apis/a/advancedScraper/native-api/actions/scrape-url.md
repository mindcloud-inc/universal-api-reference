# Scrape URL with Advanced Scraper

Retrieves scraped data from a remote URL in Advanced Scraper.

## Endpoint

- **Method:** `GET`
- **Path:** `/scraper`
- **Base URL:** `https://api.apilayer.com/adv_scraper`
- **Official documentation:** [Scrape URL](https://marketplace.apilayer.com/adv_scraper-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Remote URL to scrape. |
| `country` | query | `string` | no | Optional two-character country code for originating IP address. |
| `render` | query | `boolean` | no | Render the remote page with a browser. Set false for images, JSON, PDFs, XML, or other files. |
| `selector` | query | `string` | no | CSS selector to return only selected content. |
| `timeout` | query | `number` | no | Timeout in seconds before returning a result. APILayer documents min 5 and max 45. |
