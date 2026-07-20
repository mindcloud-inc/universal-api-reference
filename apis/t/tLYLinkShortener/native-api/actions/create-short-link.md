# Create Short Link with TLY Link Shortener

Creates a new short link in TLY Link Shortener.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/link/shorten`
- **Base URL:** `https://api.t.ly`
- **Official documentation:** [Create Short Link](https://t.ly/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `long_url` | body | `string` | yes | The destination URL to shorten. |
| `short_id` | body | `string` | no | Optional custom short code. |
| `domain` | body | `string` | no | Optional branded domain to use for the short link. |
| `description` | body | `string` | no | Optional description for the short link. |
| `public_stats` | body | `boolean` | no | Whether the short link stats should be public. |
| `expire_at_datetime` | body | `string` | no | UTC datetime when the link should expire. |
| `expire_at_views` | body | `number` | no | Maximum number of views before the link expires. |
| `password` | body | `string` | no | Optional password protecting the short link. |
| `tags[]` | body | `array<number>` | no | Optional tag IDs to associate with the short link. |
| `pixels[]` | body | `array<number>` | no | Optional pixel IDs to associate with the short link. |
