# Create Synchronous Render with Urlbox

Creates a synchronous render in Urlbox.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/render/sync`
- **Base URL:** `https://api.urlbox.com`
- **Official documentation:** [Create Synchronous Render](https://urlbox.com/docs/api#create-a-render-synchronously)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `url` | body | `string` | no |
| `html` | body | `string` | no |
| `format` | body | `string` | no |
| `width` | body | `number` | no |
| `height` | body | `number` | no |
| `full_page` | body | `boolean` | no |
| `selector` | body | `string` | no |
| `hide_cookie_banners` | body | `boolean` | no |
| `click_accept` | body | `boolean` | no |
| `block_ads` | body | `boolean` | no |
| `redirect_after` | body | `string` | no |
