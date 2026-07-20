# Update Short Link with TLY Link Shortener

Updates an existing short link in TLY Link Shortener.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/link`
- **Base URL:** `https://api.t.ly`
- **Official documentation:** [Update Short Link](https://t.ly/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `short_url` | body | `string` | yes | The short URL to update. |
| `short_id` | body | `string` | no | Optional replacement short code. |
| `long_url` | body | `string` | no | The updated destination URL. |
| `description` | body | `string` | no | Optional updated description for the short link. |
| `public_stats` | body | `boolean` | no | Whether the short link stats should be public. |
| `expire_at_datetime` | body | `string` | no | UTC datetime when the link should expire. |
| `expire_at_views` | body | `number` | no | Maximum number of views before the link expires. |
| `password` | body | `string` | no | Optional password protecting the short link. |
| `tags[]` | body | `array<number>` | no | Optional tag IDs to associate with the short link. |
| `pixels[]` | body | `array<number>` | no | Optional pixel IDs to associate with the short link. |
