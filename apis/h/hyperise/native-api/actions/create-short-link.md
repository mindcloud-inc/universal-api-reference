# Create Short Link with Hyperise

Creates a personalized short link in Hyperise.

## Endpoint

- **Method:** `POST`
- **Path:** `/short-links`
- **Base URL:** `https://app.hyperise.io/api/v1/regular`
- **Official documentation:** [Create Short Link](https://hyperise.customerly.help/en/articles/9434-Personalised-Short-Links-API)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `desc` | body | `string` | yes | The Open Graph page description. |
| `image_hash` | body | `string` | yes | The Hyperise image template hash. |
| `query_params[business_name]` | body | `string` | no | Optional personalization business name. |
| `query_params[email]` | body | `string` | no | Optional personalization email. |
| `query_params[first_name]` | body | `string` | no | Optional personalization first name. |
| `query_params[last_name]` | body | `string` | no | Optional personalization last name. |
| `query_params[website]` | body | `string` | no | Optional personalization website. |
| `title` | body | `string` | yes | The Open Graph page title. |
| `url` | body | `string` | yes | The destination URL for the short link. |
