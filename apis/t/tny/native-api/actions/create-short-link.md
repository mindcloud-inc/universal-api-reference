# Create Short Link with Tny

Creates a shortened link in Tny.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/shorten`
- **Base URL:** `https://www.tny.dev`
- **Official documentation:** [Create Short Link](https://www.tny.dev/api-docs#create-short-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `url` | body | `string` | yes | The HTTP or HTTPS URL to shorten. |
| `customSlug` | body | `string` | no | Optional custom slug. Requires a custom domain and Developer tier. |
| `domain_id` | body | `string` | no | Optional custom domain UUID for the short link. |
