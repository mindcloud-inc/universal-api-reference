# Create Asynchronous Render with Urlbox

Creates an asynchronous render in Urlbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/render/async`
- **Base URL:** `https://api.urlbox.com`
- **Official documentation:** [Create Asynchronous Render](https://urlbox.com/docs/api#create-a-render-asynchronously)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | no | The URL to render |
| `html` | body | `string` | no | The HTML to render |
| `format` | body | `string` | no | The output format of the render |
| `width` | body | `number` | no | The viewport width in pixels |
| `height` | body | `number` | no | The viewport height in pixels |
| `full_page` | body | `boolean` | no | Capture the full scrollable page |
| `selector` | body | `string` | no | Capture only the matching element selector |
| `hide_cookie_banners` | body | `boolean` | no | Automatically hide cookie banners |
| `click_accept` | body | `boolean` | no | Try to click the cookie accept button |
| `block_ads` | body | `boolean` | no | Block popular advertising networks |
