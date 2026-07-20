# Capture Screenshot with ScrapFly

Retrieves a webpage screenshot from ScrapFly.

## Endpoint

- **Method:** `GET`
- **Path:** `/screenshot`
- **Base URL:** `https://api.scrapfly.io`
- **Official documentation:** [Capture Screenshot](https://scrapfly.io/docs/screenshot-api/getting-started)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `capture` | query | `string` | no | Area to capture: viewport, full page, or a CSS selector/XPath target. |
| `format` | query | `string` | no | Image format for the returned screenshot, such as jpeg or png. |
| `resolution` | query | `string` | no | Screen resolution in WIDTHxHEIGHT format. |
| `url` | query | `string` | yes | Target URL to capture as a screenshot. |
