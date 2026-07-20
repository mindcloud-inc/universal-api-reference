# Create Screenshot with Allscreenshots

Creates a new website capture in Allscreenshots.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/screenshots`
- **Base URL:** `https://api.allscreenshots.com`
- **Official documentation:** [Create Screenshot](https://docs.allscreenshots.com/api-reference/screenshots)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The webpage URL to capture. |
| `format` | body | `string` | no | Output format such as png, jpeg, webp, or pdf. |
| `fullPage` | body | `boolean` | no | Capture the full scrollable page instead of the visible viewport. |
| `responseType` | body | `string` | no | How the screenshot result should be returned. |
| `delay` | body | `number` | no | Milliseconds to wait before capturing the page. |
| `darkMode` | body | `boolean` | no | Render the page with a dark color scheme when supported. |
| `blockAds` | body | `boolean` | no | Block common ad networks during capture. |
| `blockCookieBanners` | body | `boolean` | no | Try to hide cookie consent banners during capture. |
| `outputs[]` | body | `array<object>` | no | Optional multi-output extraction configuration. |
