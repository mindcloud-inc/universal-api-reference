# Create Screenshot from URL with PeekShot

Creates a screenshot from a URL in PeekShot.

## Endpoint

- **Method:** `POST`
- **Path:** `/screenshots`
- **Base URL:** `https://api.peekshot.com/api/v1`
- **Official documentation:** [Create Screenshot from URL](https://docs.peekshot.com/api-reference/take-screenshot-ss0c)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | body | `string` | yes | Unique project identifier. |
| `url` | body | `string` | yes | Website URL to capture. |
| `width` | body | `string` | no | Screenshot width. Docs default: 1280. |
| `height` | body | `string` | no | Screenshot height. Docs default: 1024. |
| `inject_css` | body | `string` | no | Custom CSS to apply before capture. |
| `inject_js` | body | `string` | no | Custom JavaScript to apply before capture. |
| `file_type` | body | `string` | no | Output format: jpeg, png, webp, or avif. |
| `retina` | body | `string` | no | Use true for higher-resolution screenshots. |
| `delay` | body | `string` | no | Delay in seconds before capture. Allowed range: 0 to 60. |
| `full_page` | body | `string` | no | Capture the full page instead of only the viewport. |
| `disable_javascript` | body | `string` | no | Disable page JavaScript during rendering. |
| `emulate_device` | body | `string` | no | Render the page using a supported device profile. |
| `disable_animations` | body | `string` | no | Disable animations before capture. |
| `proxy_url` | body | `string` | no | HTTP proxy URL, including authentication if needed. |
| `custom_header` | body | `string` | no | Inject a custom header into the page request. |
| `element_selector` | body | `string` | no | Target one element with a CSS selector or an xpath= expression. |
| `block_cookie_banner` | body | `string` | no | Hide cookie banners. Docs default: true. |
| `block_ads` | body | `string` | no | Block ads. Docs default: true. |
| `block_popups_by_heuristics` | body | `string` | no | Block popups heuristically. Docs default: false. |
| `cookie_template_id` | body | `string` | no | Cookie template identifier to apply. |
