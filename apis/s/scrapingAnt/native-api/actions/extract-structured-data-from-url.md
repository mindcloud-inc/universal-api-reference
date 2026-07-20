# Extract Structured Data From URL with ScrapingAnt

Retrieves AI-extracted structured data from a URL in ScrapingAnt.

## Endpoint

- **Method:** `GET`
- **Path:** `/extract`
- **Base URL:** `https://api.scrapingant.com/v2`
- **Official documentation:** [Extract Structured Data From URL](https://docs.scrapingant.com/ai-data-extraction/ai-extractor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | Fully qualified URL to scrape and extract structured data from. |
| `extract_properties` | query | `string` | yes | Free-form description of the fields to extract, such as "product title, price(number), full description". |
| `browser` | query | `boolean` | no | Enable ScrapingAnt headless browser rendering. Default is true. |
| `timeout` | query | `number` | no | Maximum request runtime in seconds. ScrapingAnt supports 5-60 seconds. |
| `proxy_type` | query | `list<string>` | no | Proxy pool type. Supported values are datacenter and residential. Accepted values: `datacenter`, `residential`. |
| `proxy_country` | query | `string` | no | Two-letter proxy country code, such as US, GB, BR, or DE. |
| `wait_for_selector` | query | `string` | no | CSS selector ScrapingAnt should wait for before returning the result. Requires browser=true. |
