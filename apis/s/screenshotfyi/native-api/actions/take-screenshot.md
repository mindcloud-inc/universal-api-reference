# Take Screenshot with screenshot.fyi

## Endpoint

- **Method:** `GET`
- **Path:** `/take`
- **Base URL:** `https://screenshot.fyi/api`
- **Official documentation:** [Take Screenshot](https://www.screenshot.fyi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | query | `string` | yes | The public webpage URL to capture. |
| `width` | query | `number` | no | Optional viewport width in pixels. |
| `height` | query | `number` | no | Optional viewport height in pixels. |
| `format` | query | `string` | no | Optional image format override. |
| `fullPage` | query | `boolean` | no | Capture the full page instead of the default viewport. |
| `darkMode` | query | `boolean` | no | Render the screenshot in dark mode when supported. |
| `disableCookieBanners` | query | `boolean` | no | Remove cookie banners and similar overlays when possible. |
