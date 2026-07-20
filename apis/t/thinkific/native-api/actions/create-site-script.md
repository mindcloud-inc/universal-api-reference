# Create Site Script with Thinkific

Creates a new site script in Thinkific.

## Endpoint

- **Method:** `POST`
- **Path:** `/site_scripts`
- **Base URL:** `https://api.thinkific.com/api/public/v1`
- **Official documentation:** [Create Site Script](https://developers.thinkific.com/api/api-documentation#/paths/~1site_scripts/post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `category` | body | `string` | yes | Site script category. |
| `content` | body | `string` | no | Inline script content (use either content or src). |
| `description` | body | `string` | yes | Site script description. |
| `load_method` | body | `string` | no | Script load method. |
| `location` | body | `string` | no | Injection location for the script. |
| `name` | body | `string` | yes | Site script name. |
| `page_scopes[]` | body | `array<string>` | yes | Pages and domains where the script should be injected. |
| `src` | body | `string` | no | External script source URL (use either src or content). |
