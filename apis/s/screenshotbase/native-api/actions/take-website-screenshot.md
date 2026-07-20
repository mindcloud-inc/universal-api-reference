# Take Website Screenshot with Screenshotbase

Captures a website screenshot with Screenshotbase.

## Endpoint

- **Method:** `GET`
- **Path:** `/take`
- **Base URL:** `https://api.screenshotbase.com/v1`
- **Official documentation:** [Take Website Screenshot](https://screenshotbase.com/docs/take)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The URL of the website you want to render. |
| `format` | query | `string` | no | The format of the image returned. |
| `quality` | query | `number` | no | The quality of the image returned for JPG or JPEG output. |
| `full_page` | query | `boolean` | no | Take a screenshot of the full page. |
| `viewport_width` | query | `number` | no | The browser viewport width in pixels. |
| `viewport_height` | query | `number` | no | The browser viewport height in pixels. |
| `ip_country_code` | query | `string` | no | ISO 3166-1 alpha-2 country code for the screenshot IP location. |
| `delay` | query | `number` | no | Seconds to wait before taking the screenshot. |
| `timeout` | query | `number` | no | The timeout in seconds for the page load. |
| `wait_until` | query | `string` | no | When the screenshot should be taken based on page load state. |
| `block_cookie_banners` | query | `boolean` | no | Block cookie banners on the page. |
| `block_ads` | query | `boolean` | no | Block ads on the page. |
| `block_chats` | query | `boolean` | no | Block chat widgets on the page. |
| `hide_selectors[]` | query | `array<string>` | no | CSS selectors to hide before taking the screenshot. |
| `styles` | query | `string` | no | Custom CSS styles to inject before taking the screenshot. |
