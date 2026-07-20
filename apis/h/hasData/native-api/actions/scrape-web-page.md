# Scrape Web Page with HasData

Retrieves scraped web page data from HasData.

## Endpoint

- **Method:** `POST`
- **Path:** `/scrape/web`
- **Base URL:** `https://api.hasdata.com`
- **Official documentation:** [Scrape Web Page](https://docs.hasdata.com/apis/web-scraping-api/quickstart)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `extractEmails` | body | `boolean` | no | Extract email addresses found on the page. |
| `extractLinks` | body | `boolean` | no | Extract links found on the page. |
| `outputFormat[]` | body | `array<string>` | no | Formats to include in the response. |
| `proxyCountry` | body | `string` | no | ISO alpha-2 country code for the proxy. |
| `proxyType` | body | `string` | no | Proxy type to use for the request. |
| `screenshot` | body | `boolean` | no | Include a rendered page screenshot. |
| `url` | body | `string` | yes | The public page URL to scrape. |
