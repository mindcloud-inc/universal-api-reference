# Scrape Website with Scrapi

Creates a website scrape job in Scrapi.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/scrape`
- **Base URL:** `https://api.scrapi.tech`
- **Official documentation:** [Scrape Website](https://scrapi.tech/docs/api_details/v1_scrape)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `useBrowser` | body | `string` | no | Use a full headless browser with JavaScript execution. |
| `responseFormat` | body | `string` | no | Response format: Json, Html, or Markdown. |
| `responseFormat` | body | `string` | no | Response format: Json, Html, or Markdown. |
| `responseSelector` | body | `string` | no | CSS or XPath selector for extracted content. |
| `responseSelector` | body | `string` | no | CSS or XPath selector for extracted content. |
| `requestMethod` | body | `string` | no | Target request method for the scrape request. |
| `requestMethod` | body | `string` | no | Target request method for the scrape request. |
| `requestBodyBase64` | body | `string` | no | Base64-encoded body for POST target requests. |
| `requestBodyBase64` | body | `string` | no | Base64-encoded body for POST target requests. |
| `useBrowser` | body | `boolean` | no | Use a full headless browser with JavaScript execution. |
| `solveCaptchas` | body | `boolean` | no | Attempt captcha solving during the scrape. |
| `includeScreenshot` | body | `boolean` | no | Include a screenshot in the scrape response. |
| `includePdf` | body | `boolean` | no | Include a PDF capture in the scrape response. |
| `includeVideo` | body | `boolean` | no | Include a video capture in the scrape response. |
| `acceptDialogs` | body | `boolean` | no | Accept popup dialogs instead of cancelling them. |
| `cookies` | body | `object` | no | Custom cookies as key/value pairs. |
| `headers` | body | `object` | no | Custom headers as key/value pairs. |
| `proxyType` | body | `string` | no | Proxy type: None, Free, Residential, DataCenter, Tor, or Custom. |
| `proxyCountry` | body | `string` | no | Proxy country key used when geotargeting. |
| `proxyCity` | body | `string` | no | Proxy city key used when geotargeting. |
| `customProxyUrl` | body | `string` | no | Custom proxy URL used when proxy type is Custom. |
| `sessionId` | body | `string` | no | Session identifier to persist state across requests. |
| `callbackUrl` | body | `string` | no | Webhook URL to receive the response asynchronously. |
